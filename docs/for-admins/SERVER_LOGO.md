# Server Logo and Branding

The FSCore *arrivals* screen shows a logo while players load in. By default that is the **FSCore wordmark**. A server owner can replace it with the community's own logo.

This is a dedicated-server feature. In single player, or on a server that sets nothing up, the FSCore wordmark simply displays and nobody is ever blocked from joining.

## How the logo reaches players

Farming Simulator 25 cannot push a custom image to players on its own, and it does not auto-download mods that are not on the ModHub. Your players need the logo file on their own PC, exactly like any other custom mod your server runs. If you already hand players a mod pack, the logo goes in it.

### Option A: bundle it in your custom map

If your server runs a custom map that players download anyway, put the logo in the root of the map's zip:

```
fscoreServerLogo.dds
```

FSCore finds it automatically. Nothing else to distribute.

### Option B: a small logo mod of your own

On a vanilla or ModHub map, make a tiny data-only mod named `FS25_FSCoreServerLogo`. FSCore looks for a mod with exactly that name and shows its logo.

```
FS25_FSCoreServerLogo/
    modDesc.xml
    img/arrivals/logo.dds
```

`modDesc.xml`:

```xml
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<modDesc descVersion="115">
    <author>Your community name</author>
    <version>1.0.0.0</version>
    <multiplayer supported="true"/>
    <title>
        <en>Server Logo</en>
    </title>
    <description>
        <en><![CDATA[Our server's logo for the FSCore arrivals screen. Data only, no scripts.]]></en>
    </description>
</modDesc>
```

1. Put your logo at `img/arrivals/logo.dds`: **800 x 488, DXT5 (BC3), no mipmaps**. To convert a PNG with [texconv](https://github.com/microsoft/DirectXTex/releases): `texconv.exe -f BC3_UNORM -m 1 -y logo.png`
2. Zip the folder's **contents** as `FS25_FSCoreServerLogo.zip`, with `modDesc.xml` at the root of the zip.
3. Put the zip in your dedicated server's mods folder, activate it and restart the server.
4. Get it to players: include it in your mod pack, or enable **Public Mod Download** in the server's web interface so they can fetch it from `http://<server-ip>:<port>/mods.html`. It is a manual install either way; the in-game download button stays greyed out for non-ModHub mods.

The mod needs no `<dependencies>` and no scripts. If FSCore is not running, it does nothing.

### Option C: a local file

A per-machine override at `modSettings/FSCore/img/arrivals/logo.dds` works on one PC without any distribution. Useful for testing, or for a host who plays on the same machine.

## Important

- **Every joining player must have the file** (the logo mod or the map) locally, or they cannot join: the server checks every non-ModHub mod.
- **Raise the version whenever you change the logo.** Overwriting the `.dds` inside a zip players already have, without raising `<version>`, causes a mod mismatch that stops them joining. For Option A, re-version your map.
- **800 x 488 matches the on-screen frame.** It is a no-mipmap UI overlay, so a size that is not a power of two is fine. To avoid a texture warning on some graphics cards, place the art on a 1024 x 512 transparent canvas instead; it then won't fill the frame exactly.
- **Keep it family friendly** and free of other people's trademarks; it is what the whole community sees.

## Which logo is shown

FSCore uses the first one it finds:

1. The `FS25_FSCoreServerLogo` mod
2. `fscoreServerLogo.dds` in the loaded custom map
3. The local override in `modSettings/FSCore/img/arrivals/logo.dds`
4. The built-in FSCore wordmark
