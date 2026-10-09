# FSCore - Server Admin Documentation

Everything you need to install, configure and run a server with FSCore.

| Document | What it covers |
|---|---|
| **[INSTALL.md](INSTALL.md)** | Installing on a dedicated server, what happens on the first load, the admin files in `modSettings`, troubleshooting |
| **[SETTINGS.md](SETTINGS.md)** | Every rule on the FSCore Settings page, what it does and its default |
| **[CONSOLE_COMMANDS.md](CONSOLE_COMMANDS.md)** | The optional `fsc*` console commands, grouped by subsystem |

## Quick start

1. Install FSCore from the GIANTS ModHub on the server and on every player's game.
2. Start the server with the mod enabled and load the save once. FSCore sets up the farms, names, colors and starting balances by itself.
3. Join as an administrator. Open the Admin Hub with **F6** to set the server name and the house rules new players see.
4. Open the pause menu, FSCore tab, to switch modules and server rules on or off. Changes apply live and are saved with the game.

No console command is needed at any point. The commands in the reference are optional tools.

## Common questions

- **"Which features can I switch off?"** The Settings page lists every module: Fishing, Boating, Pets, Scavenger, Salvaging, Clothing, Dealership, Garage, Farm Garage and Vehicle Rentals.
- **"How do I change the store and rental catalogs, the starter package or the item list?"** Edit the XML files FSCore writes to `modSettings/FSCore/` on the machine that runs the save. See [INSTALL.md](INSTALL.md).
- **"Players say their stuff disappeared after a restart."** Pull the server log for the restart and file a bug with it. FSCore saves its state with the game save, so a save that was restored from a backup also restores FSCore's data from that moment.

## Getting help

- [Issues](https://github.com/RocklandUSA/FS25_FSCore/issues) for bugs
- [Discussions](https://github.com/RocklandUSA/FS25_FSCore/discussions) for questions
