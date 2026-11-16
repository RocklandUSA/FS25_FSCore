# FSCore - Server Admin Documentation

Everything you need to install, configure and run a server with FSCore 1.0.0.0.

| Document | What it covers |
|---|---|
| **[INSTALL.md](INSTALL.md)** | Installing on a dedicated server, what happens on the first load, the admin files in `modSettings`, troubleshooting |
| **[COMMUNITY_PROJECTS.md](COMMUNITY_PROJECTS.md)** | Map layouts, Map Audit, setting out the four community projects, what each one unlocks, `fscUnlock`, the community-build rules |
| **[SETTINGS.md](SETTINGS.md)** | Every setting on the FSCore Settings page (93, including the 50 module switches), what it does and its default |
| **[CONSOLE_COMMANDS.md](CONSOLE_COMMANDS.md)** | The optional `fsc*` console commands (437), grouped by subsystem, marked admin or everyone |
| **[SERVER_LOGO.md](SERVER_LOGO.md)** | Putting your community's logo on the arrivals screen |

## Quick start

1. Install FSCore from the GIANTS ModHub on the server and on every player's game.
2. Start the server with the mod enabled and load the save once. On the base-game maps FSCore applies its map layout on the first load of a new save; on every map it sets up the farms, names, colours and starting balances by itself.
3. Join as an administrator and press **F6** for the Admin Hub. Set the server name and the house rules new players see, then open **Map Audit** to see what is placed and what is missing.
4. Set out the community projects you want (**Admin Hub > Community Projects**). Until they are built, the features they unlock stay locked; see [COMMUNITY_PROJECTS.md](COMMUNITY_PROJECTS.md).
5. Open the pause menu, **FSCore** tab, to switch modules and server rules. Changes apply live and are saved with the game.

No console command is needed at any point. The commands in the reference are optional tools.

## The Admin Hub (F6)

For an administrator, **F6** opens the Admin Hub: a directory of every admin tool, among them Map Audit, Community Projects, Stuck Vehicles + Pallets, Real Estate, Moderation (kick, ban, freeze, teleport, warn, the moderation log), Map Essentials (ATMs, vending machines, bins, seasonal street lights), the Mine, the Shiftit yard, Giggit and the delivery jobs, and the placement editors for the dealership, mechanic, garages, rentals, boat rentals, storage lockers, time clocks, doors, welcome signs, pets and zones. Players who are not administrators get the Player Hub on the same key.

## Common questions

- **"Which features can I switch off?"** Every module, on the FEATURES tab of the Settings page: 50 switches, from Fishing and Pets to the Phone, Construction, Mining and Real Estate. See [SETTINGS.md](SETTINGS.md#features).
- **"Players say the dealership is locked."** On a server with the Construction module on, FSCore's dealership, mechanic and towing calls open once the community has built the Car Dealership. Set it out, or open it by hand with `fscUnlock dealership on`. See [COMMUNITY_PROJECTS.md](COMMUNITY_PROJECTS.md).
- **"How do I change the store and rental catalogues, the starter package or the item list?"** Edit the XML files FSCore writes to `modSettings/FSCore/` on the machine that runs the save. See [INSTALL.md](INSTALL.md#admin-files-in-modsettingsfscore).
- **"Players say their stuff disappeared after a restart."** Pull the server log for the restart and file a bug with it. FSCore saves its state with the game save, so a save restored from a backup also restores FSCore's data from that moment. `fscBackups` lists the restart backups FSCore keeps.

## Getting help

- [Discord](https://discord.gg/xd9B6uSEjV) for quick questions
- [Issues](https://github.com/RocklandUSA/FS25_FSCore/issues) for bugs
- [Discussions](https://github.com/RocklandUSA/FS25_FSCore/discussions) for longer questions
