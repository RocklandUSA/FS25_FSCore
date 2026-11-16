# Map Setup and Community Projects

How an administrator gets a map ready for FSCore 1.0.0.0, checks it with **Map Audit**, and runs the **community projects** that unlock the town's big features.

## 1. The map layout

On the base-game maps (Riverbend Springs, Zielonka, Hutan Pantai, Kinlaig and Catuaí) FSCore ships a **map layout**: the NPC kiosks and sellers, zones, welcome boards, lockers, time clocks, store catalogues, garages, job locations and the server rules of a finished setup. A brand-new save on one of these maps gets its layout on the first load, before anything is built. A save that was already set up is never touched.

| Tool | What it does |
|---|---|
| `fscLayoutInfo` | Which layout file this map would use and whether one was applied |
| `fscLayoutExport [name]` | Saves your own world's setup to `modSettings/FSCore/layouts/<name>.xml` (no player data) |
| `fscLayoutApply [name] [places]` | Queues a layout for this save; it goes in at the next start. `places` = only where things stand, keeping rules, economy and players |

A file in `modSettings/FSCore/layouts/` overrides the bundled one, so a server can keep its own layout for a map, or bring one to a map FSCore does not ship a layout for.

Community projects are **not** part of a layout. On every new save an administrator sets them out (step 3).

## 2. Map Audit

**Admin Hub (`F6`) > Map Audit** is one grid of every FSCore map feature: what is placed, what is recommended (the counts of the finished Riverbend Springs layout) and a button that opens the tool that fixes it. It reads the synced data, so it shows the same on a dedicated server as in singleplayer.

Its **COMMUNITY PROJECTS** section has one row per project:

| Row shows | Meaning |
|---|---|
| Built by the community - unlocked | The project is finished; its features are open for everyone |
| Site set out - n % built, locked until finished | A site stands and is being built |
| Unlocked by an admin (`fscUnlock`) - not built yet | An administrator opened the features by hand |
| Set it out: Admin Hub > Community Projects | No site yet; the features stay locked |

While a community-project dealership is set out or built, Map Audit does not flag a missing dealership or mechanic NPC: the finished building places both itself.

## 3. Setting out a community project

1. Open **Admin Hub (`F6`) > Community Projects > PROJECTS**. Every project shows its size (stages, pieces, strikes) and an estimate of how long it takes under the current rules, for one, three and six builders.
2. Pick a project and press **SET OUT HERE**. The placement ghost appears at once: green = it fits, red = it does not. Only an administrator can set out, move or remove a community building.
3. Players build it together (see below). The same screen follows every build on the map: its stage, the builders, the wait, with **SKIP WAIT**, **FINISH NOW**, **MOVE** and **REMOVE**.

The four community projects in 1.0.0.0:

| Project | Unlocks when the community has built it | `fscUnlock` key |
|---|---|---|
| **Car Dealership** (glass showroom and drive-through service workshop) | FSCore's dealership for player-owned vehicles: buying from the sales NPC with a test drive, customising and repairing at the mechanic NPC, and the Shiftit **towing** calls. The finished building places its sales NPC behind the counter and the mechanic in the side shop | `dealership` |
| **Post Office & Parcel Depot** | The Shiftit **mail** and **parcel** rounds (they are listed but locked until then) | `postal` |
| **Self-Storage Yard** | Renting its 20 storage units: one per player (or per farm, a rule), each a big container for the backpack's items, with room for the player's crates. Rent is due every in-game month and paid to the Town; late rent brings warnings, then a locked door, then a forfeit after a grace period | `storage` |
| **Co-op Grain Elevator** (the largest build: tower-crane lifts and slip-form concrete pours) | The **Farmers Co-op**: grain sold at the elevator pays **10 % more than the best price on the map** for that crop at that moment, plus massive grain storage (the elevator's own silo, per farm). Drive the trailer or truck into the receiving lane over the dump grates, step out and press `R` at the pit. A price board on the office wall shows the co-op price against the best elsewhere | `coop` |

Rules of the unlocks:

- They are **server-wide**: once the site is finished, every player has the feature.
- Only a **community-built** site counts. The same building bought from the shop does not unlock anything.
- The game's own shop and workshop for farm machinery are never locked. Only FSCore's own features above wait for their building.
- With the **Construction** module switched off on the FSCore Settings page nothing can be built, so **nothing is locked**: every feature works as it would without community projects.
- While a feature is locked, its NPC or job says what it is waiting for: "Unlocks when the Car Dealership is built".

### Admin override: `fscUnlock`

```
fscUnlock                      the list: every key, OPEN or LOCKED, its mode and why
fscUnlock <key> on             open the feature now, built or not
fscUnlock <key> off            keep the feature locked, even when built
fscUnlock <key> auto           back to normal: open once the community has built it
```

`<key>` is `dealership`, `postal`, `storage` or `coop`. The override is checked on the server, saved with the savegame and safe to repeat. A server that wants FSCore's dealership open from day one uses `fscUnlock dealership on`.

## 4. How a community build works

- **Shifts:** every player puts one shift into a community build per day (60 strikes by default, about one big piece). The next shift opens 20 real hours after the last one started. More builders really is faster: one player alone takes about a month, a crew of four to six one to two weeks.
- **Waits:** a finished stage settles before the next one starts. The foundation's concrete cures (48 real hours by default), and Town Hall inspects every other stage (24 real hours by default).
- **Pay:** Town Hall pays a wage for the work (250 for a full shift by default) and a fee for every pallet of its materials delivered to the site (60 by default). It is a public job: it pays in full even when the town's funds are low.
- **Points and trophies:** hammering, hauling Town Hall's pallets (their value and the distance) and donating your own materials earn points. When the building is finished, every builder goes on the plaque and the top three get a Golden, Silver and Bronze Hammer trophy for their trophy cabinet at home.
- **News:** each finished stage and the finish are posted on the bulletin boards and in FarmFeed.

### The RULES tab

**Admin Hub > Community Projects > RULES** holds the server's community-build rules. They apply to every community build on the server, are saved with the savegame and have a **RESET TO DEFAULTS** button.

| What it sets | Default |
|---|---|
| Strikes per shift | 60 |
| Real hours to the next shift | 20 |
| Wait after the foundation (real hours) | 48 |
| Wait after every other stage (real hours) | 24 |
| Town Hall pay for a full shift | 250 |
| Town Hall pay per delivered pallet | 60 |
| Points per strike / per 100 hauled / per km / per 100 donated | 10 / 10 / 20 / 15 |
| Curing time (% of each piece's cure) | 100 % |
| Winter pause for curing | on |
| Grain elevator crane pieces go up by the tower crane | on (off = they are built by hand, so a server without a crane operator never stalls) |
| Crane lifts per player per day / per site per day / minutes an operator keeps the crane while someone waits | 5 / 25 / 5 |
| Man basket for high crane pieces / for the high pours | on / on |
| Full skips per slip-form lift | 4 |
| Pour spot width | 150 cm |
| Testing: short pauses (curing, inspections, shifts and crane windows) | off, 1 minute each when on |

### Useful admin commands

| Command | What it does |
|---|---|
| `fscBuildGive <plan>` | A plan and the tools for it into your backpack. Community plans: `postdepot`, `elevator`, `storageyard`, `dealership` |
| `fscBuildRush` | Clears the nearest community build's stage wait and your own shift |
| `fscBuildTestPauses on\|off`, `cure <min>`, `shift <min>` | Short construction pauses on every project for a test walk-through |
| `fscBuildFinish` / `fscBuildPiece <pieceKey\|next>` | Finish the nearest site, or put one piece in |
| `fscBuildCleanup` | Clears leftover material pallets at finished sites |
| `fscStuck` | Finds vehicles, trailers and pallets stuck in a building or under the ground, and moves or removes them |
| `fscStorageYard` | Every self-storage yard and its rented units |
| `fscElevatorLift [down]` | Ride the nearest finished grain elevator's lift |

The full list is in the [console command reference](CONSOLE_COMMANDS.md#construction-and-community-projects).

## Not in 1.0.0.0

The **Fire Station** and **Public Works** community projects are planned for 1.1 and are not part of 1.0.0.0: they are not in the community projects list or the shop. The Shiftit kerbside refuse rounds are open in 1.0.0.0 without any building.
