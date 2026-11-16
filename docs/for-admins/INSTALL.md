# Server Installation and First Start

## Requirements

- Farming Simulator 25 on PC or Mac with the latest game update (1.25.1 or newer), on the server and on every player's game.
- The same FSCore version on the server and on every client. Players who join a dedicated server download it from the ModHub like any other mod.
- Optional: the game console, only if you want to use the console commands. Nothing in FSCore requires it.

## Install

1. Download **FSCore** from the GIANTS ModHub (in game or on the ModHub website) and place the zip (do not extract it) in the server's mods folder.
2. Enable the mod in the server panel or when you create or load the save.
3. Start the server (or load your save in singleplayer).

## The first load

On the first load FSCore sets itself up:

- On Riverbend Springs, Zielonka, Hutan Pantai, Kinlaig and Catuaí a brand-new save gets FSCore's **map layout**: kiosks, NPCs, welcome boards, time clocks, garages, shops, fuel stations, job locations and the server rules of a finished setup. See [COMMUNITY_PROJECTS.md](COMMUNITY_PROJECTS.md#1-the-map-layout).
- The farms get preset names, colours and starting balances.
- The FSCore data is created inside the savegame folder and is saved together with the game from then on.
- Admin files are written to `modSettings/FSCore/` in the game's profile folder on the machine that runs the save (the dedicated server's profile, or your own PC in singleplayer). On Windows that is `Documents\My Games\FarmingSimulator2025\modSettings\FSCore\`.

Nothing has to be typed into a console. Save the game once the first load is complete.

## Set the server name and house rules

New players see the server name and the house rules in the character creator before they make their character. Change both at any time:

- In game as an administrator: **F6** opens the Admin Hub.
- Or in the console: `fscSetServerTitle <text>` and `fscSetServerRules <text>`.

## Check the map and set out the community projects

Open **Admin Hub > Map Audit** to see every FSCore map feature: what is placed, what is recommended and a button to the tool that fixes it. Then set out the community projects you want in **Admin Hub > Community Projects**. The Car Dealership, the Post Office & Parcel Depot, the Self-Storage Yard and the Co-op Grain Elevator each unlock features once the community has built them. Read [COMMUNITY_PROJECTS.md](COMMUNITY_PROJECTS.md) before you open the server: it explains what stays locked until then and how to override it.

## Modules and rules

Open the pause menu and the **FSCore** tab. The page has the tabs FEATURES, MOVEMENT, VEHICLES, ECONOMY, WORLD, INTERFACE and PLAYERS.

- **FEATURES** holds the 50 module switches. A module that is switched off stays dormant; some modules need another one (the switch text says which), and switching the needed one off turns them off too.
- **MOVEMENT**, **VEHICLES**, **ECONOMY**, **WORLD** and **INTERFACE** hold the server rules. See [SETTINGS.md](SETTINGS.md) for every rule and its default. The defaults are the setup FSCore is tested with; a few of them change standard Farming Simulator behaviour (for example the night-time fast-forward and the sleep triggers), so check them once before you open the server.
- **PLAYERS** is where an administrator looks up a player and resets their character, licences or skills.

Only administrators can change the page; everyone else sees it read-only.

## Admin files in modSettings/FSCore

| File | What it controls | Reload without a restart |
|---|---|---|
| `dealership_inventory.xml` | Vehicles sold by the FSCore dealership, their prices and card images (`img/dealership/`) | `fscDealerCatalogReload` |
| `rental_catalog.xml` | Vehicles offered by the rental kiosks and their rates | `fscRentalCatalogReload` |
| `stores.xml` | The stores and their per-store catalogues | `fscStoresReload` |
| `items.xml` | The item list: names, weights, icons (`img/items/`) | `fscItemsReload`, `fscIconsReload` |
| `welcomePackage.xml` | The starter package new players receive | restart |
| `salvaging.xml` | Salvaging buyers and prices | `fscSalvagingReloadConfig` |
| `licenses.xml` | Which vehicle classes need which licence (farm machinery, road trucks, forestry) and whether administrators are exempt | `fscLicenseReload` |
| `payroll.xml` | The wage bands for farm pay | restart |
| `layouts/<map>.xml` | Your own map layouts (`fscLayoutExport`); a file here overrides the bundled one | applied to new saves, or with `fscLayoutApply` |

FSCore writes the defaults on the first load. Edit the copy in `modSettings`, then reload with the matching console command or restart the server. ModHub updates never overwrite these files; new default entries are appended once. Older FSCore builds kept `licenses.xml` in `modSettings/FS25_FSCore/`; it is copied over automatically.

## Dedicated server notes

- Stop the server before replacing the mod zip. Restart it after every update so the server and the clients run the same version.
- After a restart, let the server finish loading before players join, and let them join one or two at a time.
- FSCore keeps `log.txt` quiet in normal play. To see its lines while you look into a problem, use `fscLogLevel info` (or create an empty file `modSettings/FSCore/logVerbose.txt` on the server and restart). Every FSCore line starts with `[FSCore`.
- FSCore keeps restart backups of its data and the farm money (`fscBackups`, `fscBackupRestore`).
- FSCore does not monitor or track anyone and sends nothing outside the game.

## Troubleshooting

| Symptom | Likely cause | What to do |
|---|---|---|
| The mod is not listed in the mod menu | The zip is in the wrong folder or was extracted | The `.zip` belongs in the `mods` folder, not extracted |
| The dealership, mechanic, mail and parcel rounds, storage units or the Farmers Co-op say "Unlocks when ... is built" | The community project is not built yet | Set it out in Admin Hub > Community Projects, or open it with `fscUnlock <key> on` |
| A player's character creator does not open | A character already exists for that account | An administrator can reset the player on the PLAYERS tab of the Settings page |
| A module is missing in game | It, or a module it needs, is switched off | Switch it on under FEATURES |
| Catalogue or item edits are not showing | The file was edited while the server was running | Reload with the matching console command or restart the server |
| Players cannot join after an update | Server and clients run different versions | Update both; the ModHub version on the server is what clients download |
