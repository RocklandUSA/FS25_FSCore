# Server Installation and First Start

## Requirements

- Farming Simulator 25 (PC), version 1.24 or newer, on the server and on every player's game.
- The same FSCore version on the server and on every client. Players who join a dedicated server download it from the ModHub like any other mod.
- Optional: the developer console, only if you want to use the console commands. Nothing in FSCore requires it.

## Install

1. Subscribe to **FSCore** on the GIANTS ModHub, or download the zip and place it (do not extract it) in the server's mods folder.
2. Enable the mod in the server panel or the game's mod menu.
3. Start the server (or load your save in singleplayer).

## The first load

On the first load FSCore sets itself up:

- The eight farms get preset names, colors and starting balances.
- The FSCore data file is created inside the savegame folder and is saved together with the game from then on.
- Admin files are written to `Documents\My Games\FarmingSimulator2025\modSettings\FSCore\` on the machine that runs the save (the dedicated server's profile folder, or your own PC in singleplayer).

Nothing has to be typed into a console. Save the game once the first load is complete.

## Set the server name and house rules

New players see the server name and the house rules on the identity screen before they create a character. Change both at any time:

- In game as an administrator: **F6** opens the Admin Hub.
- Or in the console: `fscSetServerTitle <name>` and `fscSetServerRules <text>`.

## Modules and rules

Open the pause menu and the **FSCore** tab. The page has these groups: Features, Movement, Vehicles, Economy, World, Interface and Players.

- **Features** holds the module switches (Fishing, Boating, Pets, Scavenger, Salvaging, Clothing, Dealership, Garage, Farm Garage, Vehicle Rentals). A module that is switched off stays dormant on the next load.
- The other tabs hold the server rules. See [SETTINGS.md](SETTINGS.md) for every rule and its default. Rules that change standard Farming Simulator behavior ship OFF.

## Admin files in modSettings/FSCore

| File | What it controls |
|---|---|
| `dealership_inventory.xml` | Vehicles sold by the FSCore dealership, their prices and card images (`img/dealership/`) |
| `rental_catalog.xml` | Vehicles offered by the rental kiosks and their rates |
| `items.xml` | The inventory item list: names, weights, icons |
| `welcomePackage.xml` | The starter package new players receive |
| `salvaging.xml` | Salvaging buyers and prices |
| `licenses.xml` (this one lives in `modSettings\FS25_FSCore\`) | Which vehicle classes need which license (farm machinery, road trucks, forestry) and whether administrators are exempt |

FSCore writes the defaults on the first load. Edit the copy in `modSettings`, then reload with the matching console command (for example `fscDealerCatalogReload`, `fscItemsReload`) or restart the server. ModHub updates never overwrite these files; new default entries are appended once.

## Dedicated server notes

- Stop the server before replacing the mod zip. Restart it after every update so the server and the clients run the same version.
- The server log is the first thing to pull when something goes wrong. Every FSCore line is prefixed with `[FSCore` and the subsystem name.
- FSCore does not monitor or track anyone and sends nothing outside the game.

## Troubleshooting

| Symptom | Likely cause | What to do |
|---|---|---|
| The mod is not listed in the mod menu | The zip is in the wrong folder or was extracted | The `.zip` belongs in `Documents\My Games\FarmingSimulator2025\mods\`, not extracted |
| A player's identity screen does not open | A profile already exists for that account | An administrator can reset the player from the Players tab of the Settings page |
| A module is missing in game | It is switched off on the Settings page | Switch it on under Features; it is active on the next load |
| Catalog or item edits are not showing | The file was edited while the server was running | Reload with the matching console command or restart the server |
| Players cannot join after an update | Server and clients run different versions | Update both; the ModHub version on the server is what clients download |
