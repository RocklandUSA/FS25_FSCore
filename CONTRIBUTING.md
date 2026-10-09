# Contributing to FSCore

Thanks for helping improve FSCore.

This repository hosts the **documentation and the public issue tracker** for the mod. The mod itself is closed source and is distributed only through the official GIANTS ModHub, so we do not accept code pull requests. Documentation fixes are welcome as pull requests.

## 1. File a bug report

Open an issue with the [Bug Report template](https://github.com/RocklandUSA/FS25_FSCore/issues/new?template=bug_report.yml).

A useful bug report includes:

- Your FSCore version (shown in the in-game mod menu and on the FSCore Settings page).
- Your Farming Simulator 25 version.
- Whether it happens in singleplayer, on a dedicated server, or both.
- A short numbered list of steps to reproduce it.
- The relevant lines from your `log.txt` (`Documents\My Games\FarmingSimulator2025\log.txt`).
- For dedicated servers, the matching lines from the server log.

A five-line repro with a log excerpt usually gets a fix into the next ModHub update.

## 2. Request a feature

Open an issue with the [Feature Request template](https://github.com/RocklandUSA/FS25_FSCore/issues/new?template=feature_request.yml). Describe the situation before the solution: what you want to do, why you cannot do it today, and who it helps.

Requests are weighed against the design principles of the mod:

- **Server-authoritative.** Every change is validated on the server; clients ask, the server decides.
- **Vanilla-preserving by default.** Rules that change standard Farming Simulator behavior ship OFF; administrators opt in.
- **Family friendly.** FSCore is about farming, work, services and community life.
- **One mod, optional modules.** New features should fit an existing module or be switchable off.

## 3. Server admin help

Setting up a server and the [install guide](docs/for-admins/INSTALL.md), the [settings reference](docs/for-admins/SETTINGS.md) and the [console command reference](docs/for-admins/CONSOLE_COMMANDS.md) did not answer your question? Open an issue with the [Server Admin Help template](https://github.com/RocklandUSA/FS25_FSCore/issues/new?template=server_admin_help.yml). If the docs should have answered it, that is a documentation bug and we will fix the guide.

## 4. Mod authors

Building a mod that talks to FSCore through its public API? Use the [Integration Help template](https://github.com/RocklandUSA/FS25_FSCore/issues/new?template=integration_help.yml) with the Lua you tried, what you expected and what happened. See the [modder notes](docs/for-modders/) first.

## What we cannot accept

- Pull requests that add or change mod code. The mod source is closed.
- Reverse-engineered or extracted mod code posted in issues or comments. That violates the [LICENSE](LICENSE) and the issue will be removed.
- Support requests for other mods. If another mod calls FSCore incorrectly, please raise it on that mod's tracker first.

## Code of conduct

Be respectful. Personal attacks, harassment and off-topic disputes get the issue locked. We are a small team; treating maintainers and other contributors well is the only price of admission.
