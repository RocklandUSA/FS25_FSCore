# Console Command Reference

FSCore never needs a console command to play: the mod sets itself up on the first load, and most admin tasks are also screens in the **Admin Hub (F6)**. These commands are optional administration and troubleshooting tools, typed into the game's console.

- **Admin** commands change the server, other players' data or the world. In multiplayer they are for administrators: FSCore checks the rights, and some only work on the host or the server. In singleplayer you are the administrator.
- **Everyone** commands only show information or act on your own character, vehicles, dog or crates.
- **Everyone (admin options)**: anyone can read their own figures; the options named in the help text (another player, give, set, reset) are for administrators.
- Developer probes, dumps and tests are not listed. They only exist when the game's developer controls are switched on (`game.xml`, `<development><controls>true</controls>`), which a normal server never needs.

FSCore 1.0.0.0: **437 commands** (323 admin, 114 everyone) in 48 groups.

*This page is generated from the FSCore 1.0.0.0 source; the description is the command's own help text.*

## Groups

- [Admin Hub and moderation](#admin-hub-and-moderation) (17)
- [Arrivals screen](#arrivals-screen) (1)
- [Boating](#boating) (3)
- [Bulletin board](#bulletin-board) (9)
- [Clothing](#clothing) (4)
- [Compass](#compass) (2)
- [Construction and community projects](#construction-and-community-projects) (21)
- [Core](#core) (11)
- [Crafting](#crafting) (10)
- [Dealership and mechanic](#dealership-and-mechanic) (9)
- [Doors](#doors) (8)
- [Economy and banking](#economy-and-banking) (15)
- [Employment](#employment) (9)
- [Farm dogs](#farm-dogs) (11)
- [Farm garage](#farm-garage) (6)
- [Farm Manager](#farm-manager) (9)
- [Farm store](#farm-store) (2)
- [Farming](#farming) (6)
- [Fishing](#fishing) (16)
- [Foraging](#foraging) (1)
- [Garage](#garage) (7)
- [Garden](#garden) (2)
- [Giggit and Farm Eats (mini jobs)](#giggit-and-farm-eats-mini-jobs) (29)
- [Identity and licences](#identity-and-licences) (4)
- [Interface](#interface) (5)
- [Inventory and storage](#inventory-and-storage) (25)
- [Journey and onboarding](#journey-and-onboarding) (4)
- [Lifecycle](#lifecycle) (1)
- [Mine](#mine) (13)
- [Needs](#needs) (8)
- [Placeables and NPCs](#placeables-and-npcs) (8)
- [Placement](#placement) (7)
- [Real Estate, homes and AutoPlot](#real-estate-homes-and-autoplot) (40)
- [Reputation and skills](#reputation-and-skills) (5)
- [Roads and addresses](#roads-and-addresses) (3)
- [Salvaging](#salvaging) (11)
- [Scavenger](#scavenger) (15)
- [Seats and emotes](#seats-and-emotes) (1)
- [Settings and rules](#settings-and-rules) (11)
- [Shops and fuel](#shops-and-fuel) (18)
- [Traffic vehicles](#traffic-vehicles) (1)
- [Utilities](#utilities) (2)
- [Vehicle keys and licences](#vehicle-keys-and-licences) (8)
- [Vehicle rentals](#vehicle-rentals) (11)
- [Vehicles and Shiftit](#vehicles-and-shiftit) (1)
- [Welcome boards and Town Hall](#welcome-boards-and-town-hall) (12)
- [World](#world) (3)
- [Zones](#zones) (12)

## Admin Hub and moderation

| Command | Who | What it does |
|---|---|---|
| `fscAdmin` | Admin | Open the FSCore Admin Hub - a clickable directory of every subsystem's admin page. |
| `fscBan` | Admin | fscBan <name> <hours/perm> [reason] |
| `fscBring` | Admin | fscBring <name> - bring a player to you |
| `fscFactionFarms` | Admin | Faction farms in free slots automatically. Usage: fscFactionFarms on/off |
| `fscFreeze` | Admin | fscFreeze <name> [on/off] - auto-expires after 2 min |
| `fscInitServer` | Admin | Initialise server - rename farms, set colours, set bank balances |
| `fscKick` | Admin | fscKick <name> [reason] - lounge + 2 min freeze (online players only) |
| `fscModContact` | Admin | fscModContact <text> - appeal/contact line shown to banned players |
| `fscModeration` | Admin | open the Moderation panel (admin) |
| `fscModLog` | Admin | print the last 100 moderation actions |
| `fscMyId` | Everyone | Open My ID - licences, specialisation and skill ranks |
| `fscPlayerHub` | Everyone | Open the Player Hub - the F6 directory of player tools |
| `fscResetServer` | Admin | Clear the server_initialized flag so fscInitServer can re-run |
| `fscSaveFarms` | Admin | Write faction names directly to farms.xml for persistence |
| `fscTpTo` | Admin | fscTpTo <name> - teleport yourself to a player |
| `fscUnban` | Admin | fscUnban <name> |
| `fscWarn` | Admin | fscWarn <name> <text> - phone notification + notice |

## Arrivals screen

| Command | Who | What it does |
|---|---|---|
| `fscArrivals` | Admin | Arrivals screen. Usage: fscArrivals [show/on/off/name <text>] |

## Boating

| Command | Who | What it does |
|---|---|---|
| `fscBoatRentalAdmin` | Admin | Open the Boat Rentals admin panel (NPC placement, clothing, pricing). |
| `fscBoatRentalHere` | Admin | Place the boat rental NPC at your position (face the water). |
| `fscBoatRentalRemove` | Admin | Remove the boat rental NPC. |

## Bulletin board

| Command | Who | What it does |
|---|---|---|
| `fscBoardAdd` | Admin | Add bulletin board. Usage: fscBoardAdd [name] |
| `fscBoardList` | Everyone | List all bulletin boards |
| `fscBoardNear` | Everyone | Show nearest bulletin board |
| `fscBoardRemove` | Admin | Remove a bulletin board by name |
| `fscBulletin` | Everyone | List all active bulletin posts |
| `fscBulletinPlayer` | Admin | Show posts by a player |
| `fscBulletinPrune` | Admin | Manually trigger expired post cleanup |
| `fscBulletinRemove` | Admin | Admin delete a post by ID |
| `fscBulletinStatus` | Everyone | Show post counts and next prune time |

## Clothing

| Command | Who | What it does |
|---|---|---|
| `fscClothingAdmin` | Admin | Open the Clothing admin panel (kiosk placement + NPC wardrobe). |
| `fscClothingHere` | Admin | Place a clothing kiosk at your current position. |
| `fscClothingList` | Everyone | List all placed clothing kiosks. |
| `fscClothingRemove` | Admin | Remove a clothing kiosk: fscClothingRemove <gid> |

## Compass

| Command | Who | What it does |
|---|---|---|
| `fscCompass` | Everyone | Show compass status |
| `fscCompassReset` | Everyone | Reset compass settings to defaults |

## Construction and community projects

| Command | Who | What it does |
|---|---|---|
| `fscBuildCleanup` | Admin | clear the leftover material pallets + hardware boxes at every FINISHED building site (community projects: their Town Hall pallets) |
| `fscBuildCure` | Admin | the nearest building site's concrete is cured at once (curing pause over) |
| `fscBuildFinish` | Admin | finish the nearest unfinished building site at once (every piece in) |
| `fscBuildGive` | Admin | a Garden shed plan, a hammer + trowel, the hardware and the shed's pallets. fscBuildGive <compost/woodstore/pergola/coop/greenhouse/postdepot/elevator/storageyard/dealership>: that plan instead |
| `fscBuildPiece` | Admin | ONE piece of the nearest unfinished building site goes in - the one being built. fscBuildPiece <pieceKey/next> [siteId] |
| `fscBuildRemove` | Admin | remove the nearest building site (owner / admin) |
| `fscBuildRush` | Admin | clear the nearest community build's stage wait and your own shift |
| `fscBuildTestPauses` | Admin | short construction pauses on every project - curing + inspections (houses too), the next shift + crane windows; 1 min each unless set; running ones cut. fscBuildTestPauses on/off / cure <min> / shift <min> / <min> (both) |
| `fscBuildWhy` | Everyone | what this machine holds for the nearest building site (fscBuildWhy rebuild: draw it again) |
| `fscCoopChickens` | Everyone | the nearest chicken coop's live FS25 chickens - nav mesh, husbandry, why not |
| `fscElevatorLift` | Admin | ride the nearest finished Co-op Grain Elevator's lift to its roof from anywhere (fscElevatorLift down: to its foot) |
| `fscHouseGrass` | Admin | meadow back on the bare ground round a finished house built from a blueprint (the house itself stays bare). fscHouseGrass [radius m, default 60] = the nearest / all = every one / list [radius / all] = dry run |
| `fscManBasket` | Admin | the nearest crane site's man basket. fscManBasket [here/home/status]: here = set down beside you, home = its staging spot, status = what this machine sees |
| `fscPalletFit` | Everyone | the planks / wood beam / cement pallets near you - layer shown + collision top on this machine |
| `fscPalletGive` | Admin | one materials pallet 5 m ahead. Usage: fscPalletGive <fill type on a pallet, e.g. PLANKS, CEMENT, BREAD, FLOUR, BOARDS> [amount] |
| `fscStorageYard` | Admin | every self storage yard on the map + its rented units (renter, paid / late / locked, arrears, door) |
| `fscStuck` | Admin | vehicles, trailers + pallets stuck in a building or under the ground. fscStuck [scan] = list only (dry run) / list / move <n> [yes] / remove <n> [yes] (twice) / aim |
| `fscSupplyYard` | Admin | set the nearest general store's supply yard here [spots] - stand where the forklift drives in, facing the row |
| `fscSupplyYardRemove` | Admin | remove the nearest supply yard |
| `fscSupplyYardShow` | Everyone | outline the supply yards near you for a minute |
| `fscUnlock` | Admin | community-project unlocks. fscUnlock = the list / fscUnlock <dealership/postal/storage/coop> on/off/auto (auto = open once the community has built it) |

## Core

| Command | Who | What it does |
|---|---|---|
| `fscBackupRestore` | Admin | Restore a restart backup at the next start. Usage: fscBackupRestore <n> (0 cancels) |
| `fscBackups` | Admin | List the restart backups (FSCore data + farm money at each of the last 3 starts) |
| `fscDataSizes` | Everyone | the data store's size - every namespace / scope / key, biggest first |
| `fscLayoutApply` | Admin | Queue a layout for this save - it goes in at the next start. 'places' = only where things stand (keeps rules, economy, players). Usage: fscLayoutApply [name] [places] |
| `fscLayoutExport` | Admin | Export this world's layout (NPCs, zones, kiosks, boards, catalogues, rules) to modSettings/FSCore/layouts/<name>.xml. Usage: fscLayoutExport [name] |
| `fscLayoutInfo` | Everyone | Which layout file this map would use and whether one was applied |
| `fscLoanClear` | Admin | remove one loan record. Usage: fscLoanClear <loanId> (see fscLoans) |
| `fscLoans` | Admin | list every loan on the server |
| `fscPerf` | Admin | server performance paths on/off - off restores the original behaviour (fscPerf on/off) |
| `fscSave` | Admin | Force immediate save |
| `fscStatus` | Everyone | Show status and registered namespaces |

## Crafting

| Command | Who | What it does |
|---|---|---|
| `fscCrafting` | Everyone | List all crafting recipes |
| `fscCraftingGive` | Admin | Admin: execute craft for player (bypass checks) |
| `fscCraftingScan` | Admin | Re-run the scene-graph scan for vanilla workbench/forge/cooking props |
| `fscCraftingStation` | Admin | Manage crafting stations (add/remove/list/near) |
| `fscRecipeAdd` | Admin | Add custom recipe: fscRecipeAdd <id> <stationType> <cashCost> <label...> |
| `fscRecipeInput` | Admin | Add input to recipe: fscRecipeInput <recipeId> <itemId> [qty] |
| `fscRecipeList` | Everyone | List all recipes (default + custom) |
| `fscRecipeOutput` | Admin | Add output to recipe: fscRecipeOutput <recipeId> <itemId> [qty] |
| `fscRecipeRemove` | Admin | Remove custom recipe: fscRecipeRemove <recipeId> |
| `fscRecipeReq` | Admin | Add requirement: fscRecipeReq <recipeId> <skill> <level> |

## Dealership and mechanic

| Command | Who | What it does |
|---|---|---|
| `fscDealerAutoParkStatus` | Everyone | Show every active spawn and its owner's offline duration. |
| `fscDealerCatalogList` | Everyone | Print every inventory entry currently loaded. |
| `fscDealerCatalogReload` | Admin | Re-read modSettings/FSCore/dealership_inventory.xml. |
| `fscDealerCatalogWriteDefaults` | Admin | Overwrite modSettings/FSCore/dealership_inventory.xml with bundled defaults. |
| `fscDealerKioskHere` | Admin | Place the dealership kiosk at your current position. |
| `fscDealerKioskRemove` | Admin | Remove the dealership (despawns NPC, interaction, hotspot). |
| `fscDealerOwned` | Admin | fscDealerOwned <userId/me> |
| `fscDealerPurgeFlags` | Admin | Scrub orphan transient marker flags around the dealership kiosk. Usage: fscDealerPurgeFlags [radius_m] (default 100m). |
| `fscDealershipAdmin` | Admin | Open the Dealership admin panel (kiosk placement + per-vehicle list price overrides). |

## Doors

| Command | Who | What it does |
|---|---|---|
| `fscDoorAdd` | Admin | Create a door, capturing OUTSIDE anchor at your feet: fscDoorAdd <name> |
| `fscDoorAdmin` | Admin | Open the Doors admin panel |
| `fscDoorInside` | Admin | Set the INSIDE anchor of a door at your feet: fscDoorInside <name> |
| `fscDoorList` | Everyone | List all doors and their anchor status |
| `fscDoorOutside` | Admin | Re-set the OUTSIDE anchor of a door at your feet: fscDoorOutside <name> |
| `fscDoorRemove` | Admin | Delete a door: fscDoorRemove <name/id> |
| `fscDoorRename` | Admin | Rename a door: fscDoorRename <name/id> <new name> |
| `fscDoorStep` | Admin | Step forward through a solid wall/door to set the inside anchor: fscDoorStep [meters] |

## Economy and banking

| Command | Who | What it does |
|---|---|---|
| `fscATMAdd` | Admin | Register ATM at current position. Usage: fscATMAdd [name] |
| `fscATMAdmin` | Admin | Open the Map Essentials panel (ATMs, vending machines, trash cans) |
| `fscATMList` | Admin | List all registered ATM locations |
| `fscATMNear` | Admin | Show nearest ATM to your position |
| `fscATMScan` | Admin | find every ATM on the map and give it a prompt |
| `fscBankAdd` | Admin | Register Bank at current position. Usage: fscBankAdd [name] |
| `fscBankList` | Admin | List all registered Bank locations |
| `fscBankNear` | Admin | Show nearest Bank to your position |
| `fscCoords` | Everyone | Show player world coordinates |
| `fscEconBankAdd` | Admin | Deposit to current account. Usage: fscEconBankAdd <userId/me> <amount> |
| `fscEconCashAdd` | Admin | Grant cash. Usage: fscEconCashAdd <userId/me> <amount> |
| `fscEconReconstructLoans` | Admin | Walk Dealership.owned and re-create any DealershipLoan whose loanId is missing from LoanManager (recovers orphaned references from saves predating the loan-persistence fix). |
| `fscEconSave` | Admin | Force an immediate save of all economy data |
| `fscEconStatus` | Everyone | Show current wallet balances and FSCore status |
| `fscHolidayLights` | Admin | street-light holiday decorations [christmas/winter/harvest/newyear/halloween/spring/lunar/summer/farm/carnival/off] or mode <manual/game/real> or hemisphere <auto/north/south> or skip/include <theme> or rescan or showcase [radius/off] (no argument = status) |

## Employment

| Command | Who | What it does |
|---|---|---|
| `fscClockHere` | Admin | Place a time-clock interaction point at your position |
| `fscClockIn` | Everyone | Clock into a job (default: farming) |
| `fscClockOut` | Everyone | Clock out of your current job |
| `fscClockRate` | Admin | Set a generic job's pay: fscClockRate <jobId> <base> <work> |
| `fscClockStatus` | Everyone | Show your current shift + registered jobs |
| `fscFarmWage` | Farm owner / manager | Owner/Manager: set your farm wage. fscFarmWage <non_driving/driving/field> <rate> |
| `fscFarmWages` | Everyone | Show your farm's wage rates + the server bands |
| `fscPayrollBand` | Admin | Set a wage band: fscPayrollBand <tier> <min> <max> |
| `fscTimeClockAdmin` | Admin | Open the Time Clock kiosk admin panel |

## Farm dogs

| Command | Who | What it does |
|---|---|---|
| `fscPet` | Everyone | status / summon your dog |
| `fscPetBall` | Everyone | drop a fresh ball at you |
| `fscPetBonus` | Admin | set the dog farm-duty animal bonus % (0-100) |
| `fscPetBowl` | Everyone | place / pick up the dog bowl |
| `fscPetBreed` | Everyone | 1 Labrador / 2 Border Collie |
| `fscPetCoat` | Everyone | set coat for current dog type |
| `fscPetDismiss` | Admin | remove your dog |
| `fscPetPrice` | Admin | set a Pet Shelter price - fscPetPrice <id> <price> |
| `fscPetPurgeUser` | Admin | delete a user's pet data - fscPetPurgeUser <uniqueUserId> |
| `fscPetRecover` | Admin | un-stick a glitched/invisible dog (re-seat + show) |
| `fscPetStoreEdit` | Admin | open the Pet Shelter seller placement/clothing editor |

## Farm garage

| Command | Who | What it does |
|---|---|---|
| `fscFarmGarageAdmin` | Admin | Open the Farm Garage admin panel (per-farm machinery/attachments kiosks). |
| `fscFarmGarageHere` | Admin | Place a farm garage kiosk: fscFarmGarageHere <machinery/attach> <farmId 1-8> |
| `fscFarmGarageList` | Everyone | List all placed farm garage kiosks. |
| `fscFarmGarageMyFarm` | Everyone | Print your current farmId. |
| `fscFarmGarageRegistry` | Admin | Print the stored-vehicle registry: fscFarmGarageRegistry [farmId] |
| `fscFarmGarageRemove` | Admin | Remove a farm garage kiosk: fscFarmGarageRemove <machinery/attach> <farmId 1-8> |

## Farm Manager

| Command | Who | What it does |
|---|---|---|
| `fscFarmAdmin` | Everyone (farm managers edit) | Open the Farm Manager panel (members / hire / access rules) |
| `fscFarmBlock` | Admin | Block a player. Usage: fscFarmBlock <userId/stateId/me> [reason] |
| `fscFarmHire` | Admin | Hire a lounge player. Usage: fscFarmHire <userId/stateId/me> |
| `fscFarmManager` | Everyone | List farm members and roles |
| `fscFarmManagerInit` | Admin | (Admin only) Set yourself as farm owner |
| `fscFarmReconcile` | Admin | Re-sync FSCore roles to vanilla farm membership |
| `fscFarmSet` | Admin | Set a server setting. Usage: fscFarmSet <key> <on/off/number> |
| `fscFarmSettings` | Everyone | List FarmManager server settings + current values |
| `fscFarmUnblock` | Admin | Unblock a player. Usage: fscFarmUnblock <userId/stateId/me> |

## Farm store

| Command | Who | What it does |
|---|---|---|
| `fscFarmStoreCollect` | Admin | the Farm Storage Barns collect their farms' pallets now, part-filled too, and say what is in range (admin) |
| `fscMilkHouse` | Everyone | the milk houses, their tanks and the farm barns in range (read-only) |

## Farming

| Command | Who | What it does |
|---|---|---|
| `fscFarmWorkAch` | Everyone (admin options) | your medals (<player> / give <line> <tier> [player] = admins; lines = the list) |
| `fscFarmWorkRank` | Everyone (admin options) | your rank, Farm Points and the way to the next rank (<player> / set <1-15> [player] = admins) |
| `fscFarmWorkReset` | Admin | reset awards/all <player/all> [confirm] (admins) |
| `fscFarmWorkSet` | Everyone (admin options) | xp on/off, scale <25-300>, ai <0/25/50> (admins); no argument = show |
| `fscFarmWorkStats` | Everyone (admin options) | your farm work counters (fscFarmWorkStats <player> / all = admins) |
| `fscFarmWorkWeek` | Everyone (admin options) | the week and the Farmer of the Week (end / post = admins, for testing) |

## Fishing

| Command | Who | What it does |
|---|---|---|
| `fscFish` | Everyone | Fishing rod status (equip the rod in a utility slot to fish) |
| `fscFishBoardAdmin` | Admin | fscFishBoardAdmin -- open the marina board admin panel (placement / leaderboard / tournaments) |
| `fscFishBoardMove` | Admin | fscFishBoardMove -- (multi-board) use the F6 admin panel to select + nudge a board |
| `fscFishBoardPlace` | Admin | fscFishBoardPlace -- ADD a marina bulletin board at your position + heading (multi-board) |
| `fscFishBoardRemove` | Admin | fscFishBoardRemove -- remove ALL marina bulletin boards |
| `fscFishBuyerAdmin` | Admin | fscFishBuyerAdmin -- open the Fish Buyer admin panel (place / wardrobe / prices) |
| `fscFishBuyerMove` | Admin | fscFishBuyerMove -- re-place the Fish Buyer NPC at your current position |
| `fscFishBuyerPlace` | Admin | fscFishBuyerPlace -- place the Fish Buyer NPC at your current position |
| `fscFishBuyerRemove` | Admin | fscFishBuyerRemove -- remove the Fish Buyer NPC |
| `fscFishSellerAdmin` | Admin | fscFishSellerAdmin -- open the Fish Seller admin panel (place / wardrobe / prices) |
| `fscFishSellerMove` | Admin | fscFishSellerMove -- re-place the Fish Seller NPC at your current position |
| `fscFishSellerPlace` | Admin | fscFishSellerPlace -- place the Fish Seller NPC at your current position |
| `fscFishSellerRemove` | Admin | fscFishSellerRemove -- remove the Fish Seller NPC |
| `fscFishTrophyAward` | Admin | re-award every fishing record trophy from the records (safe to repeat) |
| `fscFishTrophyInfo` | Everyone | who holds each fishing record trophy |
| `fscFishTrophyTest` | Admin | a test record catch. Usage: fscFishTrophyTest <species> [player/me] [lengthCm] [weightKg] |

## Foraging

| Command | Who | What it does |
|---|---|---|
| `fscForageHere` | Admin | grow a mushroom cluster next to you: fscForageHere [chanterelle/porcini/morel] |

## Garage

| Command | Who | What it does |
|---|---|---|
| `fscGarageAddHere` | Admin | Place a garage at your current position: fscGarageAddHere [id] |
| `fscGarageAdmin` | Admin | Open the Garage admin panel (multi-garage placement + slot-cap settings). |
| `fscGarageList` | Everyone | List all placed garages. |
| `fscGarageNuke` | Admin | Force-remove a stubborn garage entry by tostring-matching its key. Usage: fscGarageNuke <gid-as-displayed> |
| `fscGaragePurgeFlags` | Admin | Scrub orphan transient marker flags around a garage. Usage: fscGaragePurgeFlags <gid/all> [radius_m] (default 100m). |
| `fscGarageRemove` | Admin | Remove a specific garage: fscGarageRemove <id> |
| `fscGarageRemoveAll` | Admin | Remove every placed garage. |

## Garden

| Command | Who | What it does |
|---|---|---|
| `fscGardenGive` | Admin | raised bed plans, tools, brackets, soil, seeds, fertiliser, a watering can + plank / beam pallets |
| `fscGardenGrow` | Admin | the garden squares within 20 m grow <days> now |

## Giggit and Farm Eats (mini jobs)

| Command | Who | What it does |
|---|---|---|
| `fscJobComplete` | Admin | Admin complete: fscJobComplete <userId/stateId/me> |
| `fscJobExpire` | Admin | Expire a job: fscJobExpire <jobId> |
| `fscJobGenerate` | Admin | Force job generation cycle |
| `fscJobLocation` | Admin | Manage locations: fscJobLocation add/remove/list/near [name] |
| `fscJobs` | Everyone | List all jobs on the board |
| `fscJobsPlayer` | Admin | Show player job state: fscJobsPlayer <userId/stateId/me> |
| `fscJunkClear` | Admin | Clear junk offers: fscJunkClear [offerId/all] |
| `fscJunkList` | Everyone | List junk offers, claimed piles + settings |
| `fscJunkPay` | Admin | Set junk pay: fscJunkPay <itemPay> <bonusPct> |
| `fscJunkSpawn` | Admin | Create a junk cleanup offer: fscJunkSpawn [here/zoneName] |
| `fscMiniJobsAdd` | Admin | Add a pickup site of any registered job type at your position: fscMiniJobsAdd <type> [label] [npcKey] (see fscMiniJobsTypes) |
| `fscMiniJobsClearCooldowns` | Admin | Clear Farm Eats cooldowns: fscMiniJobsClearCooldowns [all/decline/completion] |
| `fscMiniJobsClearScanLocations` | Admin | Wipe scan-added delivery locations (manual entries kept): fscMiniJobsClearScanLocations [all/house/production] |
| `fscMiniJobsDeliveryAdmin` | Admin | Open the MiniJobs Delivery admin panel |
| `fscMiniJobsList` | Everyone | List all pickup sites (id, type, label, position) |
| `fscMiniJobsPurgeOrphans` | Admin | Scan for and despawn orphan cargo pallets matching any job-type xml |
| `fscMiniJobsRemove` | Admin | Remove a pickup site: fscMiniJobsRemove <id> |
| `fscMiniJobsScanLocations` | Admin | Scan map for houses + production points and add as delivery locations: fscMiniJobsScanLocations [dedupDistanceMeters=5] |
| `fscMiniJobsSweep` | Admin | Force a stale-delivery sweep right now: fscMiniJobsSweep [ttlSeconds] |
| `fscMowDebug` | Everyone (admin options) | the mowing job's cut count on this machine AND the server (MP: your own shift, or admins) |
| `fscMowProbe` | Everyone | the grass, land and job where you stand / drive |
| `fscRolloffDisposeTest` | Admin | set a test pallet / box down in the nearest roll-off [pallet/box] |
| `fscRolloffFee` | Admin | tipping fee per item in the game's currency, 0 = free (small x0.5, large x1.5) |
| `fscRolloffInfo` | Admin | the nearest roll-off - who is there, what is inside and why it stays |
| `fscRolloffList` | Everyone | list the disposal roll-offs + the tipping fee |
| `fscStopCheck` | Everyone | delivery stops nobody can use (drop-offs, letterboxes) - fscStopCheck [all = check again] |
| `fscWashClear` | Admin | Admin: clear the power-wash board and the washed list |
| `fscWashList` | Everyone | List power-wash offers |
| `fscWashOffer` | Admin | Admin: put the washable building nearest you on the Giggit board |

## Identity and licences

| Command | Who | What it does |
|---|---|---|
| `fscGrantLicense` | Admin | Admin grant licence. Usage: fscGrantLicense <userId/stateId/me> <licenseId> |
| `fscIdentity` | Everyone | Show your identity card |
| `fscLicenses` | Everyone | List your licences |
| `fscRevokeLicense` | Admin | Admin revoke licence. Usage: fscRevokeLicense <userId/stateId/me> <licenseId> |

## Interface

| Command | Who | What it does |
|---|---|---|
| `fscHotspotShots` | Admin | photograph every FSCore map icon's place for its map picture. fscHotspotShots [list/stop/all/<filter>] [dist m] [yaw deg] [eye m] |
| `fscIconsPath` | Admin | Print the modSettings folder path where admin icon files belong. |
| `fscIconsReload` | Admin | Invalidate the item-icon cache so re-resolution picks up newly-added DDS files in modSettings/FSCore/img/items/ |
| `fscIconsReseed` | Admin | Re-copy bundled item icons into modSettings/FSCore/img/items/. Optional arg 'force' overwrites admin edits. |
| `fscMoneyHudReset` | Admin | Panic-clear every active money-HUD suppressor (use if an admin UI crashed mid-open and the wallet HUD is stuck off). |

## Inventory and storage

| Command | Who | What it does |
|---|---|---|
| `fscClearProps` | Admin | Remove all spawned props (optionally filter: fscClearProps [kind]) |
| `fscClothesLockerHere` | Admin | Place a clothing locker (change into saved outfits) at your position |
| `fscContainerRecall` | Everyone | Recall a container pallet to your position: fscContainerRecall [id/label/type] (nearest if omitted) |
| `fscInv` | Everyone | Show your own inventory |
| `fscInvBuyFridge` | Everyone | Buy refrigerator storage at current spot (price 8000, 75kg, 1 per player): fscInvBuyFridge [label] |
| `fscInvBuyShelves` | Everyone | Buy shelves storage at current spot (price 5000, 100kg, 1 per player): fscInvBuyShelves [label] |
| `fscInvClearPin` | Everyone | Clear PIN on nearest crate |
| `fscInvContainerNear` | Everyone | Show nearest container |
| `fscInvContainers` | Everyone | List all world containers |
| `fscInvGive` | Admin | Give item to yourself: fscInvGive <itemId> [qty] |
| `fscInvGiveTo` | Admin | Give item to another player: fscInvGiveTo <userId/stateId/me> <itemId> [qty] |
| `fscInvItems` | Everyone | List all registered item types |
| `fscInvPlayer` | Admin | Show another player's inventory: fscInvPlayer <userId/stateId/me> |
| `fscInvSetPin` | Everyone | Set PIN on nearest crate: fscInvSetPin <pin> |
| `fscInvShare` | Everyone | Share nearest crate with player: fscInvShare <userId> |
| `fscInvUnshare` | Everyone | Revoke crate access: fscInvUnshare <userId> |
| `fscItemsPath` | Admin | Print the modSettings folder + items.xml path for the admin |
| `fscItemsReload` | Admin | Re-read modSettings/FSCore/items.xml and re-register every item |
| `fscItemsWriteDefaults` | Admin | Overwrite modSettings/FSCore/items.xml with the bundled defaults (LOSES customisations) |
| `fscListProps` | Everyone | List spawned props with their world positions |
| `fscLockerHere` | Admin | Place a locker row at your position |
| `fscLockerList` | Everyone | List placed locker rows |
| `fscLockerNudge` | Admin | Fine-tune a locker: fscLockerNudge <id> <x/y/z/heading> <delta> |
| `fscLockerRemove` | Admin | Remove a locker row: fscLockerRemove <id> |
| `fscStorageAdmin` | Admin | Open the storage container (locker) admin panel |

## Journey and onboarding

| Command | Who | What it does |
|---|---|---|
| `fscHintsReset` | Everyone | Forget seen lightbulb hints so they fire again. Usage: fscHintsReset [hintId] |
| `fscOnboardingGive` | Admin | Force-deliver the starter package to a player |
| `fscOnboardingReset` | Admin | Clear a player's starter-package-received flag |
| `fscOnboardingShow` | Admin | Print the current starter package contents |

## Lifecycle

| Command | Who | What it does |
|---|---|---|
| `fscLifecycle` | Admin | Lifecycle management: fscLifecycle [action] [args] |

## Mine

| Command | Who | What it does |
|---|---|---|
| `fscMineAddHits` | Admin | add strikes to the rock face (testing). Usage: fscMineAddHits [n] |
| `fscMineBoost` | Admin | every strike on the rock counts x times until the server restarts (testing). Usage: fscMineBoost <1-100> |
| `fscMineCartGive` | Admin | 20 rail sections + a mine cart into your bag |
| `fscMineCartTop` | Admin | a mine cart on the rails at the mine entrance |
| `fscMineDown` | Admin | take the lift down |
| `fscMineDust` | Admin | the rock dust at the face - colour + alpha (live). Usage: fscMineDust [grey] [alpha] |
| `fscMineHits` | Admin | strikes a rock section needs, rolled between min and max (live). Usage: fscMineHits <min> <max> |
| `fscMineInfo` | Admin | where the mine is, how far it is dug |
| `fscMineLantern` | Admin | the mine lanterns - light brightness, reach + the flame's glow (live, this machine). Usage: fscMineLantern [gain] [range] [glow] [halo] |
| `fscMineNewMaze` | Admin | open the next shaft now (as if a new year began) |
| `fscMinePlace` | Admin | place the mine entrance 4 m in front of you (a new shaft below it) |
| `fscMineRemove` | Admin | remove the mine entrance |
| `fscMineSweat` | Admin | energy + water 100 strikes cost (live). Usage: fscMineSweat <energy> <water> |

## Needs

| Command | Who | What it does |
|---|---|---|
| `fscNeeds` | Everyone | Show your current hunger/thirst needs |
| `fscNeedsPlayer` | Admin | Show needs for a player: fscNeedsPlayer <userId/stateId/me> |
| `fscNeedsRefill` | Admin | Refill needs: fscNeedsRefill <userId/stateId/me> |
| `fscNeedsSet` | Admin | Set needs: fscNeedsSet <userId/stateId/me> <hunger> <thirst> [fatigue] |
| `fscRestAdd` | Admin | Add rest point at player position: fscRestAdd [name] |
| `fscRestList` | Everyone | List all rest points |
| `fscRestNear` | Everyone | Find nearest rest point |
| `fscRestRemove` | Admin | Remove a custom rest point: fscRestRemove <name> |

## Placeables and NPCs

| Command | Who | What it does |
|---|---|---|
| `fscNpcEdit` | Admin | Open NPC editor UI. Usage: fscNpcEdit <name> |
| `fscOutfit` | Admin | Change NPC clothing. Usage: fscOutfit <name> <slot> <item> [color] |
| `fscOutfitSlots` | Everyone | List clothing slots/items on NPC. Usage: fscOutfitSlots <name> [slot] |
| `fscPlace` | Admin | Place object at current position. Usage: fscPlace <type> [name] [degrees] |
| `fscPlaceList` | Everyone | List all placed objects |
| `fscPlaceNear` | Everyone | List placed objects near you. Usage: fscPlaceNear [radius] |
| `fscPlaceTypes` | Everyone | List all available placeable types |
| `fscRemove` | Admin | Remove a placed object. Usage: fscRemove <name> |

## Placement

| Command | Who | What it does |
|---|---|---|
| `fscPropCatalog` | Everyone | List every prop key the spawner knows (atm, trashcan, vendingmachine, mailbox, gas tanks, ...) |
| `fscPropClear` | Admin | Remove every prop you've spawned (does NOT touch map-placed props) |
| `fscPropList` | Everyone | List every prop you've spawned with its id + position |
| `fscPropNear` | Everyone | List spawned props within N metres of the player (default 2m). Usage: fscPropNear [radius] |
| `fscPropPurgeKey` | Admin | Remove every persisted prop matching a catalogue key. One-shot cleanup for orphan kiosk flags. Usage: fscPropPurgeKey <key> |
| `fscPropRemove` | Admin | Remove a spawned prop. Usage: fscPropRemove <propId> |
| `fscPropSpawn` | Admin | Spawn a prop at your position. Usage: fscPropSpawn <key> (see fscPropCatalog) |

## Real Estate, homes and AutoPlot

| Command | Who | What it does |
|---|---|---|
| `fscDecorLineup` | Admin | Every Home Decor piece in numbered rows in front of you (this machine only, nothing saved): fscDecorLineup [all/<category>/<from #>] / clear |
| `fscDriveway` | Admin | Driveways from the garage to the car gate: fscDriveway [list/lay/remove] [all] (list = dry run; lay = homes without one, free; remove = meadow back) |
| `fscFenceInfo` | Admin | Fences on this machine: runs in the synced store per plot, how many stand, any not built and why |
| `fscHouseAdd` | Admin | New home: look at its front door - fscHouseAdd <layout> <price> [name] |
| `fscHouseAdmin` | Admin | Open the Real Estate editor (also in the Admin Hub) |
| `fscHouseDepth` | Admin | Interior depth below the door: fscHouseDepth <home> <-20..-100> |
| `fscHouseDoor` | Admin | Move a home's front door to the one you look at: fscHouseDoor <home> |
| `fscHouseEvict` | Admin | Put an owned home back on the market: fscHouseEvict <home> |
| `fscHouseGarage` | Admin | Home garage at your feet, cars come out the way you look: fscHouseGarage <home> [clear] |
| `fscHouseGoto` | Admin | Go to a home's front door: fscHouseGoto <home> |
| `fscHouseLabel` | Admin | Own name instead of the address: fscHouseLabel <home> <name> (no name = the address again) |
| `fscHouseLand` | Everyone | What the game sees as land where you stand (land id, owner farm, yours?) + every home's land |
| `fscHouseLayout` | Admin | Interior: fscHouseLayout <home> <S1/S2/A/M2/L1/T1> |
| `fscHouseList` | Everyone | List the homes |
| `fscHouseListing` | Admin | Take a home off / put it on the market: fscHouseListing <home> <on/off> |
| `fscHouseLot` | Admin | Walk a home's plot: fscHouseLot <home> / done / cancel / clear <home> / set <home> <x,z;x,z;...> |
| `fscHousePlotProbe` | Admin | Log every object inside a home's plot (map, traffic, placeables): fscHousePlotProbe <home> |
| `fscHousePrice` | Admin | fscHousePrice <home> <price> |
| `fscHouseProbe` | Admin | Inside a home: log what is around you (16 directions, knee + chest height) |
| `fscHouseRemove` | Admin | Delete a home (not owned): fscHouseRemove <home> |
| `fscHouseServerProbe` | Admin | Inside a home on a server: the server's view (its interior, doors, your position, what blocks ahead) into your log |
| `fscHouseSign` | Admin | FOR SALE sign at your feet, facing the way you look: fscHouseSign <home> [clear] |
| `fscLotCheck` | Admin | The one-house rule on a lot (this machine + the server, map house scanned again): fscLotCheck [lot] [clearmap] |
| `fscLotFinish` | Admin | Skip a lot's house build ahead: fscLotFinish [lot] [stage/all] |
| `fscLotList` | Everyone | List the building lots, their owner and what stands on them |
| `fscLotNew` | Admin | New building lot on a Town Hall field: fscLotNew walk <price> [name] (then fscHouseLot done) / fscLotNew here <price> <width> [depth] [name] |
| `fscLotPlan` | Admin | A house plan in your bag: fscLotPlan <ranchhouse/harvesthouse> |
| `fscLotRemove` | Admin | Delete a lot (empty, not owned): fscLotRemove [lot] (default: the one you stand in) |
| `fscMowerGrid` | Everyone | Robot mower: in a yard, show for 60 s why each spot is mowed or skipped (green mowed, grey no grass, yellow past the plot outline, blue decor / building, red solid) |
| `fscPlotLawn` | Admin | LAWN: MEADOW - meadow grass at mowing height inside a plot's lines (crop grass + bare natural ground; never paving, paths, buildings or anything placed): fscPlotLawn <home/lot> |
| `fscPlotLawnUndo` | Admin | Put a plot's ground back the way LAWN: MEADOW found it (crop grass / bare ground): fscPlotLawnUndo <home/lot/all> |
| `fscSubdivBuild` | Admin | AutoPlot: build the plan you see (streets, lots, signs, lawns) |
| `fscSubdivCancel` | Admin | AutoPlot: drop the plan you see (nothing was changed) |
| `fscSubdivCleanup` | Admin | AutoPlot: take down what removed lots / subdivisions left behind (their fences) and drop missing lots from their subdivision |
| `fscSubdivHydrants` | Admin | AutoPlot: a subdivision's hydrant type (default: the map's region - MapUS / MapEU / MapAS, a mod map US): fscSubdivHydrants [sd1] <us/eu/as> [model 1-4] |
| `fscSubdivInfo` | Admin | AutoPlot: the plan you see (every lot) + the subdivisions built |
| `fscSubdivPlan` | Admin | AutoPlot: plan the field you stand on: fscSubdivPlan [frontage 32] [depth 55] [front yard 8] [price 45000] [entry edge 1] [level 0/1] [auto/across/along] [lots/homes/mix] [picket/none/<fence style key>] [rotate 0/180] [auto/hammer/circle/none] |
| `fscSubdivStreetLights` | Admin | AutoPlot: street lights (lightPole02) + fire hydrants along a built subdivision's streets - once, a second run adds nothing: fscSubdivStreetLights [sd1] (default: the one you stand in, else the newest) |
| `fscSubdivToggle` | Admin | AutoPlot: a planned lot's next choice (lots: off / on; homes + mix: lot -> each house -> off): fscSubdivToggle <lot number> |
| `fscSubdivUndo` | Admin | AutoPlot: undo a subdivision - its unsold empty lots go (no lot left: streets back to earth): fscSubdivUndo [sd1] (default: the one you stand in, else the newest) |

## Reputation and skills

| Command | Who | What it does |
|---|---|---|
| `fscRep` | Everyone | Show your reputation levels |
| `fscRepGive` | Admin | Admin grant XP. Usage: fscRepGive <userId/stateId/me> <skill> <amount> |
| `fscRepLeaderboard` | Everyone | Show top 10 for a skill. Usage: fscRepLeaderboard <skill> |
| `fscRepPlayer` | Everyone | Show reputation for a player. Usage: fscRepPlayer <userId/stateId/me> |
| `fscRepReset` | Admin | Admin reset player reputation. Usage: fscRepReset <userId/stateId/me> |

## Roads and addresses

| Command | Who | What it does |
|---|---|---|
| `fscGps` | Everyone | turn-by-turn directions on the HUD on / off (this machine) |
| `fscRoadScan` | Admin | find + name this map's roads (from its traffic network) and save them to modSettings/FSCore/roads |
| `fscRoadShow` | Everyone | draw the named roads around you (toggle) |

## Salvaging

| Command | Who | What it does |
|---|---|---|
| `fscSalvageBuyerAdmin` | Admin | fscSalvageBuyerAdmin -- open the Salvage Buyer admin panel (place / wardrobe / prices) |
| `fscSalvageBuyerMove` | Admin | fscSalvageBuyerMove -- re-place the Salvage Buyer NPC at your current position |
| `fscSalvageBuyerPlace` | Admin | fscSalvageBuyerPlace -- place the Salvage Buyer NPC at your current position |
| `fscSalvageBuyerRemove` | Admin | fscSalvageBuyerRemove -- remove the Salvage Buyer NPC |
| `fscSalvagingClearCooldowns` | Admin | Admin: clear every container's cooldown |
| `fscSalvagingConfigPath` | Everyone | Print the modSettings paths the config loader uses |
| `fscSalvagingCount` | Admin | Print discovered + cooldown counts |
| `fscSalvagingList` | Admin | List discovered containers with world positions |
| `fscSalvagingReloadConfig` | Admin | Re-read modSettings/FSCore/salvaging.xml + re-register items |
| `fscSalvagingScan` | Admin | Scan map for trash / salvaging / debris containers |
| `fscSalvagingStatus` | Everyone | Print which inventory + economy providers we resolved |

## Scavenger

| Command | Who | What it does |
|---|---|---|
| `fscGnomePreview` | Admin | the current and the new garden gnome side by side in front of you (local visual only). Usage: fscGnomePreview [clear] |
| `fscScavengerAdmin` | Admin | Toggle the Scavenger admin control panel |
| `fscScavengerAuto` | Admin | Automatic seasonal hunts. Usage: fscScavengerAuto [on/off/now] |
| `fscScavengerCredit` | Admin | credit finds to yourself on the leaderboard. Usage: fscScavengerCredit <typeId> <count> <tag> |
| `fscScavengerHide` | Admin | Hide every active spawn from the PDA map |
| `fscScavengerPlaceCollector` | Admin | Place the collector NPC at your feet, facing your direction |
| `fscScavengerRemoveCollector` | Admin | Remove the collector NPC |
| `fscScavengerReset` | Admin | Reset - same as Stop today; will also wipe per-player collected counts once persistence ships |
| `fscScavengerReveal` | Admin | Reveal every active spawn on the PDA map |
| `fscScavengerScan` | Admin | Drop PDA preview hotspots on N legal spawn points (NO spawn). Usage: fscScavengerScan <count> |
| `fscScavengerScanClear` | Admin | Clear all scan-preview hotspots |
| `fscScavengerStart` | Admin | Start a scavenger event. Usage: fscScavengerStart [typeId] [count] |
| `fscScavengerStats` | Everyone | Scavenger leaderboard, running hunts and the last results. Usage: fscScavengerStats [reset] |
| `fscScavengerStatus` | Everyone | Scavenger status |
| `fscScavengerStop` | Admin | Stop the active event (despawns remaining items + hotspots) |

## Seats and emotes

| Command | Who | What it does |
|---|---|---|
| `fscEmote` | Everyone | play an emote. Usage: fscEmote <wave/crossed/hips/shrug/think/salute/clap/lean/stop> |

## Settings and rules

| Command | Who | What it does |
|---|---|---|
| `fscConfig` | Everyone | Show all rule states |
| `fscNpcNear` | Everyone | list every scene object within N m of you (default 4) - finds leftover NPC parts |
| `fscNpcSpots` | Everyone | how many ambient NPC spots the map has / remove_npcs took out |
| `fscResetServerRules` | Admin | Reset the server rules text to the FSCore default |
| `fscRules` | Everyone | List all available rule IDs |
| `fscSetRule` | Admin | Set rule value (fscSetRule <ruleId> <value>) |
| `fscSetServerRules` | Admin | Set the server rules text (fscSetServerRules <text>) |
| `fscSetServerTitle` | Admin | Set the Character Creation popup title (fscSetServerTitle <text>) |
| `fscSweepProduction` | Admin | Manually trigger the production_storage_only sweep |
| `fscToggle` | Admin | Toggle a rule (fscToggle <ruleId>) |
| `fscTradeIn` | Everyone | What the shop pays for the vehicle you are in, with the trade-in breakdown |

## Shops and fuel

| Command | Who | What it does |
|---|---|---|
| `fscPumpAdd` | Admin | fscPumpAdd "<label>" -- stamp a fuel_station at player's current position (public/road fuel by default) |
| `fscPumpHere` | Everyone | fscPumpHere -- list any registered fuel_station within 5m of the player |
| `fscServices` | Admin | fscServices <list/add/remove/catalog/fuel/probe> [args] |
| `fscServicesFuelPolicy` | Admin | fscServicesFuelPolicy <locationId> <farm/public> -- mark a fuel_station as farm (blocks personal vehicles) or public (anyone) |
| `fscServicesProbeNearby` | Everyone | fscServicesProbeNearby [radius] -- dump every placeable + activatable object near the player (default 30m). Use to diagnose fuel-pump detection. |
| `fscServicesRemoveByLabel` | Admin | Remove EVERY store location whose label matches the argument. Usage: fscServicesRemoveByLabel Cooler |
| `fscServicesScanFuel` | Admin | fscServicesScanFuel [--register] [--verbose] -- scan map for fuel pumps (placeables + LoadTriggers); --register auto-adds fuel_station locations |
| `fscServicesVendingList` | Everyone | List every node the vending scanner has matched, with its name + position |
| `fscServicesVendingReset` | Admin | Remove all scanner-registered vending/cooler locations and clear the scanner cache (use to retune patterns) |
| `fscServicesVendingScan` | Admin | Scan the map for vending machines / coolers and auto-register each as a general store |
| `fscStoreAdd` | Admin | fscStoreAdd [name] -- adds a general_store at player pos with walk-up shopping |
| `fscStoreList` | Everyone | fscStoreList -- list every general_store location |
| `fscStoreNear` | Everyone | fscStoreNear -- show nearest store + whether player is in trigger range |
| `fscStoreRemove` | Admin | fscStoreRemove <name/locationId> -- remove a general_store |
| `fscStoresReload` | Admin | fscStoresReload -- re-read modSettings/FSCore/stores.xml and apply per-store catalogue overrides |
| `fscStoresWriteDefaults` | Admin | fscStoresWriteDefaults -- overwrite modSettings/FSCore/stores.xml with current stores + default catalogues |
| `fscVendingHideNear` | Admin | Hide the vending machine nearest you (decor / unreachable) - never registered again, saved with the map layout. Usage: fscVendingHideNear [radiusM=25] |
| `fscVendingUnhideAll` | Admin | Bring back every hidden vending machine (they register on the next scan / restart) |

## Traffic vehicles

| Command | Who | What it does |
|---|---|---|
| `fscRollbackWhy` | Everyone | what the rollback bed prompts see from where you stand (stand at the control box) |

## Utilities

| Command | Who | What it does |
|---|---|---|
| `fscLogLevel` | Everyone | Show or set the FSCore log level (error/warn/info/debug) |
| `fscPlayableHere` | Everyone | is this spot inside the playable area (the objective spawn test) |

## Vehicle keys and licences

| Command | Who | What it does |
|---|---|---|
| `fscLicense` | Admin | Admin licence. Usage: fscLicense <userId/stateId/me> grant/revoke/show <car/tractor/heavy/licenseId> |
| `fscLicenseClass` | Everyone | Which licence the vehicle you're in (or nearest) needs, and why |
| `fscLicenseReload` | Admin | Admin re-read modSettings/FSCore/licenses.xml and push it to all clients |
| `fscVehicleKey` | Everyone | Give spare key. Usage: fscVehicleKey <stateId> |
| `fscVehicleKeyRevoke` | Everyone | Revoke spare key. Usage: fscVehicleKeyRevoke <stateId> |
| `fscVehicleKeys` | Everyone | List your locked vehicles and keys |
| `fscVehicleLock` | Everyone | Lock the vehicle you're in |
| `fscVehicleUnlock` | Everyone | Unlock the vehicle you're in |

## Vehicle rentals

| Command | Who | What it does |
|---|---|---|
| `fscRentalAdmin` | Admin | Open the Vehicle Rentals admin panel (kiosk placement + per-vehicle pricing). |
| `fscRentalCatalogList` | Everyone | Print every catalogue entry currently loaded (key, price, deposit, availability). |
| `fscRentalCatalogReload` | Admin | Re-read modSettings/FSCore/rental_catalog.xml and re-register every rental vehicle. |
| `fscRentalCatalogWriteDefaults` | Admin | Overwrite modSettings/FSCore/rental_catalog.xml with the bundled defaults (LOSES customisations). |
| `fscRentalKioskHere` | Admin | Place the APE Rentals kiosk at your current position. |
| `fscRentalKioskRemove` | Admin | Remove the rental kiosk (despawns NPC, interaction, hotspot). |
| `fscRentalPurgeFlags` | Admin | Scrub orphan transient marker flags around the kiosk. Usage: fscRentalPurgeFlags [radius_m] (default 100m). |
| `fscRentalPurgeOrphans` | Admin | Scan for and despawn orphan rental vehicles near the kiosk (server-only). |
| `fscRentalReturn` | Admin | Force-return a rental: fscRentalReturn <userId/me> |
| `fscRentalStatus` | Everyone | Show all active rentals. |
| `fscRentalSweep` | Admin | Force a stale-rental sweep right now (server-only, no deposit refund). |

## Vehicles and Shiftit

| Command | Who | What it does |
|---|---|---|
| `fscVehicle` | Admin | Vehicle management: fscVehicle <action> [args] |

## Welcome boards and Town Hall

| Command | Who | What it does |
|---|---|---|
| `fscWelcome` | Everyone | Welcome board: fscWelcome list/inspect <articleId> |
| `fscWelcomeAdd` | Admin | Add article: fscWelcomeAdd <category> <title> |
| `fscWelcomeBoard` | Admin | Board mgmt: fscWelcomeBoard add/remove/list/near [name] |
| `fscWelcomeBoardPrint` | Admin | Printed welcome boards: fscWelcomeBoardPrint [on/off] (admin; no argument = show) |
| `fscWelcomeDelete` | Admin | Delete article: fscWelcomeDelete <articleId> |
| `fscWelcomeGift` | Everyone | Show gift config |
| `fscWelcomePin` | Admin | Toggle pin: fscWelcomePin <articleId> |
| `fscWelcomeResetClaim` | Admin | Reset claim: fscWelcomeResetClaim <userId/stateId/me> |
| `fscWelcomeResetSeen` | Admin | Reset seen: fscWelcomeResetSeen <userId/stateId/me> |
| `fscWelcomeSetArticle` | Admin | Set welcome article: fscWelcomeSetArticle <articleId> |
| `fscWelcomeSetGift` | Admin | Set gift: fscWelcomeSetGift <itemId> <qty> [<itemId> <qty> ...] |
| `fscWelcomeSignAdmin` | Admin | Open the Welcome Signs admin panel (spawn / rename / move signs). |

## World

| Command | Who | What it does |
|---|---|---|
| `fscBoar` | Everyone | Wild boar: fscBoar - list detected boar herds + whether on your land |
| `fscLand` | Everyone | Land ownership: fscLand [farmId] - owned parcels + fields |
| `fscSpeedZone` | Admin | Speed zones: fscSpeedZone add/remove/list/probe [args] |

## Zones

| Command | Who | What it does |
|---|---|---|
| `fscPolyZoneAdd` | Admin | fscPolyZoneAdd <name> [w h d] -- stamp a box at player pos (default 2x2x2m, base on ground) |
| `fscPolyZoneEdit` | Admin | fscPolyZoneEdit -- open the in-game zone editor (right-side panel; pick a zone on the left, nudge position/yaw/size with arrows; ESC or X to close) |
| `fscPolyZoneHide` | Admin | fscPolyZoneHide -- disable debug wireframe rendering |
| `fscPolyZoneList` | Admin | fscPolyZoneList -- print every registered zone |
| `fscPolyZoneMove` | Admin | fscPolyZoneMove <name> -- move zone to player's current position (keeps size/yaw) |
| `fscPolyZoneNear` | Admin | fscPolyZoneNear -- print the nearest zone and the camera-aimed zone |
| `fscPolyZoneOcclusion` | Admin | fscPolyZoneOcclusion [on/off] -- depth-tested box (objects hide edges behind them) vs always-on-top. Default on. |
| `fscPolyZoneRemove` | Admin | fscPolyZoneRemove <name> |
| `fscPolyZoneShow` | Admin | fscPolyZoneShow -- enable debug wireframe rendering (toggle off with fscPolyZoneHide) |
| `fscPolyZoneSize` | Admin | fscPolyZoneSize <name> <w> <h> <d> -- set half-extents in metres (so full size = 2xeach) |
| `fscPolyZoneTeleport` | Admin | fscPolyZoneTeleport <name> -- jump the player to the zone's centre |
| `fscPolyZoneYaw` | Admin | fscPolyZoneYaw <name> <degrees> -- rotate zone around vertical axis |

