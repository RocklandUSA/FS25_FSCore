# Console Command Reference

FSCore does not need any console command to play: the mod sets itself up on the first load. These commands are optional administration and troubleshooting tools. They require Farming Simulator's developer console (enable it in `game.xml`, then press the console key in game). Commands that change server state, other players' data or the world are admin-only; a non-admin player can only read their own data.

Total: **434 commands**, grouped by subsystem.

## Admin Hub

| Command | Description |
|---|---|
| `fscAdmin` | Open the FSCore Admin Hub — a clickable directory of every subsystem's admin page. |
| `fscAdminProbe` | FSCore: Admin diagnostic dump |
| `fscBan` | FSCore: fscBan <name> <hours/perm> [reason] |
| `fscBring` | FSCore: fscBring <name> - bring a player to you |
| `fscFactionFarms` | FSCore: Faction farms in free slots automatically. Usage: fscFactionFarms on/off |
| `fscFreeze` | FSCore: fscFreeze <name> [on/off] - auto-expires after 2 min |
| `fscInitServer` | FSCore: Initialize server — rename farms, set colors, set bank balances |
| `fscKick` | FSCore: fscKick <name> [reason] - lounge + 2 min freeze (online players only) |
| `fscModContact` | FSCore: fscModContact <text> - appeal/contact line shown to banned players |
| `fscModLog` | FSCore: print the last 100 moderation actions |
| `fscModeration` | FSCore: open the Moderation panel (admin) |
| `fscMyId` | FSCore: Open My ID — licences, specialization and skill ranks |
| `fscPlayerHub` | FSCore: Open the Player Hub — the F6 directory of player tools |
| `fscResetServer` | FSCore: Clear the server_initialized flag so fscInitServer can re-run |
| `fscSaveFarms` | FSCore: Write faction names directly to farms.xml for persistence |
| `fscTpTo` | FSCore: fscTpTo <name> - teleport yourself to a player |
| `fscUnban` | FSCore: fscUnban <name> |
| `fscWarn` | FSCore: fscWarn <name> <text> - phone notification + notice |

## Arrivals screen

| Command | Description |
|---|---|
| `fscArrivals` | FSCore: Arrivals screen. Usage: fscArrivals [show/on/off/name <text>] |

## Boating

| Command | Description |
|---|---|
| `fscBoatAnchor` | FSCore Boating: toggle anchor on the nearest boat (anchored = no drift) |
| `fscBoatDrive` | FSCore Boating: toggle driving the nearest boat (forward throttle) |
| `fscBoatProbe` | FSCore: raycast from the camera and NAME whatever you're looking at (asset identification) |
| `fscBoatRemove` | FSCore Boating: remove the nearest boat |
| `fscBoatRentalAdmin` | Open the Boat Rentals admin panel (NPC placement, clothing, pricing). |
| `fscBoatRentalHere` | Place the boat rental NPC at your position (face the water). |
| `fscBoatRentalRemove` | Remove the boat rental NPC. |
| `fscBoatSpawn` | FSCore Boating: spawn a bass boat ahead of you (aim at water) |
| `fscBoatSteer` | FSCore Boating: steer the boat you're driving: fscBoatSteer <-1..1> (0 = straight) |
| `fscProbeDown` | FSCore: raycast straight DOWN from you (what's under your feet: terrain/water/object) |

## Bulletin board

| Command | Description |
|---|---|
| `fscBoardAdd` | Add bulletin board. Usage: fscBoardAdd [name] |
| `fscBoardList` | List all bulletin boards |
| `fscBoardNear` | Show nearest bulletin board |
| `fscBoardProbe` | Diagnostic: bulletin system status |
| `fscBoardRemove` | Remove a bulletin board by name |
| `fscBulletin` | List all active bulletin posts |
| `fscBulletinPlayer` | Show posts by a player |
| `fscBulletinPrune` | Manually trigger expired post cleanup |
| `fscBulletinRemove` | Admin delete a post by ID |
| `fscBulletinStatus` | Show post counts and next prune time |

## Clothing

| Command | Description |
|---|---|
| `fscClothingAdmin` | Open the Clothing admin panel (kiosk placement + NPC wardrobe). |
| `fscClothingDumpSlots` | Dump the catalog for each slot on the local player's style. |
| `fscClothingHere` | Place a clothing kiosk at your current position. |
| `fscClothingList` | List all placed clothing kiosks. |
| `fscClothingProbe` | Diagnose which PlayerStyle path resolves on the local player. |
| `fscClothingRemove` | Remove a clothing kiosk: fscClothingRemove <gid> |

## Compass

| Command | Description |
|---|---|
| `fscCompass` | Show compass status |
| `fscCompassProbe` | Compass diagnostic probe |
| `fscCompassReset` | Reset compass settings to defaults |

## Settings and rules

| Command | Description |
|---|---|
| `fscConfig` | FSCoreConfig: Show all rule states |
| `fscFinanceProbe` | FSCoreConfig: Dump Farm + finance-frame methods (find loan API) |
| `fscManualAttachDiag` | Diagnose why manual_attach isn't finding a target near you |
| `fscMapProbe` | FSCoreConfig: Dump map-frame methods + actions (find teleport surfaces) |
| `fscMenuInject` | FSCore: Re-run sidebar page registration (debug) |
| `fscMenuProbe` | FSCore: Probe sidebar page registration state |
| `fscNpcNear` | FSCore: list every scene object within N m of you (default 4) - finds leftover NPC parts |
| `fscNpcSpots` | FSCore: how many ambient NPC spots the map has / remove_npcs took out |
| `fscNpcXmlProbe` | FSCoreConfig: Dump vanilla NPC XML (build whitelist source) |
| `fscProbe` | FSCoreConfig: Probe game classes (fscProbe npc/shop/hud/console) |
| `fscProbeAnimals` | Dump Animal Dealer / Animal Screen API methods |
| `fscProbeAttacherJoints` | Dump AttacherJoints API + nearest vehicle's joint structure |
| `fscProbeCheat` | Find money/cheat/teleport console-command method names |
| `fscProbeConsole` | List console commands matching optional filter (usage: fscProbeConsole money) |
| `fscProbeFarmland` | Dump farmland-purchase API methods for disable_field_buying forensics |
| `fscProbeFlight` | Dump player fields for flight-mode forensics |
| `fscProbeGameSettings` | Dump GameSettings.SETTING keys related to motor/start/engine |
| `fscProbeMotorizedMethods` | Dump Motorized class method names matching motor/start/auto/ignition |
| `fscProbeProduction` | Dump ProductionPoint API + first production placeable for storage-mode forensics |
| `fscProbeShop` | Dump shop/vehicle-purchase API methods for disable_menu_shopping forensics |
| `fscProbeStrength` | Dump player physics fields for super-strength forensics |
| `fscProbeStrengthLive` | Print live spec_hands super-strength fields |
| `fscProbeTour` | Dump guided-tour-related fields (run while tour popup is visible) |
| `fscProbeVehicle` | Dump motor/enter fields on current vehicle for forensics |
| `fscResetServerRules` | FSCoreConfig: Reset the server rules text to the FSCore default |
| `fscRules` | FSCoreConfig: List all available rule IDs |
| `fscSetRule` | FSCoreConfig: Set rule value (fscSetRule <ruleId> <value>) |
| `fscSetServerRules` | FSCoreConfig: Set the server rules text (fscSetServerRules <text>) |
| `fscSetServerTitle` | FSCoreConfig: Set the Character Creation popup title (fscSetServerTitle <text>) |
| `fscSurfaceProbe` | FSCore: what you stand on + its collision layer (finds surfaces small props fall through) |
| `fscSweepProduction` | Manually trigger the production_storage_only sweep |
| `fscTestDamage` | Set nearest motorized vehicle's damage % (default 100 = totaled) |
| `fscTestFatigue` | Set local player's fatigue % (default 5 = depleted, <30 = warning) |
| `fscTestMoneyCheat` | Directly invoke the money-cheat method to test the block |
| `fscTimeManagerStatus` | Print FSCoreTimeManager current decision + inputs |
| `fscToggle` | FSCoreConfig: Toggle a rule (fscToggle <ruleId>) |
| `fscTradeIn` | FSCoreConfig: What the shop pays for the vehicle you are in, with the trade-in breakdown |

## Core

| Command | Description |
|---|---|
| `fscBackupRestore` | FSCore: Restore a restart backup at the next start. Usage: fscBackupRestore <n> (0 cancels) |
| `fscBackups` | FSCore: List the restart backups (FSCore data + farm money at each of the last 3 starts) |
| `fscDump` | FSCore: Dump namespace data. Usage: fscDump namespace [farmId] |
| `fscGet` | FSCore: Get a value. Usage: fscGet namespace key [farmId] |
| `fscLayoutApply` | FSCore: Queue a layout for this save - it goes in at the next start. 'places' = only where things stand (keeps rules, economy, players). Usage: fscLayoutApply [name] [places] |
| `fscLayoutExport` | FSCore: Export this world's layout (NPCs, zones, kiosks, boards, catalogs, rules) to modSettings/FS25_FSCore/layouts/<name>.xml. Usage: fscLayoutExport [name] |
| `fscLayoutInfo` | FSCore: Which layout file this map would use and whether one was applied |
| `fscLoanClear` | FSCore (admin): remove one loan record. Usage: fscLoanClear <loanId> (see fscLoans) |
| `fscLoans` | FSCore (admin): list every loan on the server |
| `fscPerf` | FSCore: server performance paths on/off - off restores the original behaviour (fscPerf on/off) |
| `fscSave` | FSCore: Force immediate save |
| `fscStatus` | FSCore: Show status and registered namespaces |

## Crafting

| Command | Description |
|---|---|
| `fscCrafting` | List all crafting recipes |
| `fscCraftingGive` | Admin: execute craft for player (bypass checks) |
| `fscCraftingProbe` | Diagnostic: recipe/station/Interaction status |
| `fscCraftingScan` | Re-run the scene-graph scan for vanilla workbench/forge/cooking props |
| `fscCraftingStation` | Manage crafting stations (add/remove/list/near) |
| `fscRecipeAdd` | Add custom recipe: fscRecipeAdd <id> <stationType> <cashCost> <label...> |
| `fscRecipeInput` | Add input to recipe: fscRecipeInput <recipeId> <itemId> [qty] |
| `fscRecipeList` | List all recipes (default + custom) |
| `fscRecipeOutput` | Add output to recipe: fscRecipeOutput <recipeId> <itemId> [qty] |
| `fscRecipeRemove` | Remove custom recipe: fscRecipeRemove <recipeId> |
| `fscRecipeReq` | Add requirement: fscRecipeReq <recipeId> <skill> <level> |

## Dealership

| Command | Description |
|---|---|
| `fscDealerActiveProbe` | Diagnostic: dump the per-process active-spawn state (userId, position, distance to kiosk). |
| `fscDealerAutoParkStatus` | Show every active spawn and its owner's offline duration. |
| `fscDealerCatalogList` | Print every inventory entry currently loaded. |
| `fscDealerCatalogReload` | Re-read modSettings/FSCore/dealership_inventory.xml. |
| `fscDealerCatalogWriteDefaults` | Overwrite modSettings/FSCore/dealership_inventory.xml with bundled defaults. |
| `fscDealerForceAutoPark` | Mark <userId/me> as offline (overrides the 15-min buffer) and run the auto-park sweep immediately. Use again with same arg to clear the override. |
| `fscDealerKioskHere` | Place the dealership kiosk at your current position. |
| `fscDealerKioskRemove` | Remove the dealership (despawns NPC, interaction, hotspot). |
| `fscDealerOwned` | Usage: fscDealerOwned <userId/me> |
| `fscDealerProcessPayments` | Force the weekly payment-processing tick now (debug). |
| `fscDealerPurgeFlags` | Scrub orphan transient marker flags around the dealership kiosk. Usage: fscDealerPurgeFlags [radius_m] (default 100m). |
| `fscDealershipAdmin` | Open the Dealership admin panel (kiosk placement + per-vehicle list price overrides). |

## Diagnostics

| Command | Description |
|---|---|
| `fscAnimPlay` | FSCore: play a clip on the nearest NPC. Usage: fscAnimPlay <set> <clip> |
| `fscAnimProbe` | FSCore: list cached animation clips + your skeleton into the log |
| `fscAnimStop` | FSCore: return the nearest NPC to idle |
| `fscBoneTest` | FSCore: turn one bone of your character. Usage: fscBoneTest <bone> <x/y/z> <degrees> [free] / stop |
| `fscEmoteTest` | FSCore: play a clip from fsc_emotes.i3d on you. Usage: fscEmoteTest <clip/stop> |
| `fscMemDiff` | FSCore: Diff two memory samples. Usage: fscMemDiff <tagA> <tagB> |
| `fscMemSample` | FSCore: Snapshot Lua heap + namespace entry counts. Usage: fscMemSample [tag] |
| `fscMemSampleServer` | FSCore: Trigger fscMemSample on the SERVER (lands in server log.txt). Usage: fscMemSampleServer [tag] |
| `fscStateDump` | FSCore: Full one-line-per-key dump for cross-machine diff. Usage: fscStateDump [namespace] |
| `fscStateDumpServer` | FSCore: Trigger fscStateDump on the SERVER (lands in server log.txt). Usage: fscStateDumpServer [namespace] |
| `fscStateHash` | FSCore: Hash local DataStore for desync detection. Usage: fscStateHash [namespace] |
| `fscStateHashServer` | FSCore: Trigger fscStateHash on the SERVER (lands in server log.txt). Usage: fscStateHashServer [namespace] |

## Doors

| Command | Description |
|---|---|
| `fscDoorAdd` | [admin] Create a door, capturing OUTSIDE anchor at your feet: fscDoorAdd <name> |
| `fscDoorAdmin` | FSCore: Open the Doors admin panel |
| `fscDoorInside` | [admin] Set the INSIDE anchor of a door at your feet: fscDoorInside <name> |
| `fscDoorList` | List all doors and their anchor status |
| `fscDoorOutside` | [admin] Re-set the OUTSIDE anchor of a door at your feet: fscDoorOutside <name> |
| `fscDoorRemove` | [admin] Delete a door: fscDoorRemove <name/id> |
| `fscDoorRename` | [admin] Rename a door: fscDoorRename <name/id> <new name> |
| `fscDoorStep` | [admin] Step forward through a solid wall/door to set the inside anchor: fscDoorStep [meters] |
| `fscDoorTP` | Teleport yourself INSIDE a door (test): fscDoorTP <name/id> |

## Economy

| Command | Description |
|---|---|
| `fscATMAdd` | FSCore: Register ATM at current position. Usage: fscATMAdd [name] |
| `fscATMList` | FSCore: List all registered ATM locations |
| `fscATMNear` | FSCore: Show nearest ATM to your position |
| `fscBankAdd` | FSCore: Register Bank at current position. Usage: fscBankAdd [name] |
| `fscBankList` | FSCore: List all registered Bank locations |
| `fscBankNear` | FSCore: Show nearest Bank to your position |
| `fscCoords` | FSCore: Show player world coordinates |
| `fscEconBankAdd` | FSCore (admin): Deposit to current account. Usage: fscEconBankAdd <userId/me> <amount> |
| `fscEconCashAdd` | FSCore (admin): Grant cash. Usage: fscEconCashAdd <userId/me> <amount> |
| `fscEconReconstructLoans` | FSCore (admin): Walk Dealership.owned and re-create any DealershipLoan whose loanId is missing from LoanManager (recovers orphaned references from saves predating the loan-persistence fix). |
| `fscEconSave` | FSCore: Force an immediate save of all economy data |
| `fscEconStatus` | FSCore: Show current wallet balances and FSCore status |

## Economy (ATM and bank)

| Command | Description |
|---|---|
| `fscATMAdmin` | FSCore: Open the Map Essentials panel (ATMs, vending machines, trash cans) |
| `fscATMScan` | FSCore: find every ATM on the map and give it a prompt |

## Employment

| Command | Description |
|---|---|
| `fscClockDebug` | Live pay-detection breakdown: tier reasoning + minutes/$ per tier this shift |
| `fscClockHere` | [admin] Place a time-clock interaction point at your position |
| `fscClockIn` | Clock into a job (default: farming) |
| `fscClockOut` | Clock out of your current job |
| `fscClockRate` | [admin] Set a generic job's pay: fscClockRate <jobId> <base> <work> |
| `fscClockStatus` | Show your current shift + registered jobs |
| `fscFarmWage` | Owner/Manager: set your farm wage. fscFarmWage <non_driving/driving/field> <rate> |
| `fscFarmWages` | Show your farm's wage rates + the server bands |
| `fscPayrollBand` | [server] Set a wage band: fscPayrollBand <tier> <min> <max> |
| `fscTimeClockAdmin` | FSCore: Open the Time Clock kiosk admin panel |

## Farm garage

| Command | Description |
|---|---|
| `fscFarmGarageAdmin` | Open the Farm Garage admin panel (per-farm machinery/attachments kiosks). |
| `fscFarmGarageDumpItem` | Dump storeItem fields for the first stored record (or all): fscFarmGarageDumpItem [farmId] |
| `fscFarmGarageDumpOutfit` | Dump every outfit slot + item list for a kiosk's NPC: fscFarmGarageDumpOutfit <gid> |
| `fscFarmGarageHere` | Place a farm garage kiosk: fscFarmGarageHere <machinery/attach> <farmId 1-8> |
| `fscFarmGarageList` | List all placed farm garage kiosks. |
| `fscFarmGarageMyFarm` | Print your current farmId. |
| `fscFarmGarageRegistry` | Print the stored-vehicle registry: fscFarmGarageRegistry [farmId] |
| `fscFarmGarageRemove` | Remove a farm garage kiosk: fscFarmGarageRemove <machinery/attach> <farmId 1-8> |

## Farm Manager

| Command | Description |
|---|---|
| `fscFarmApi` | FSCore: Probe available vanilla farm-transition methods (introspection) |
| `fscFarmBlock` | FSCore: Block a player. Usage: fscFarmBlock <userId/stateId/me> [reason] |
| `fscFarmDiag` | FSCore: Diagnose vanilla-vs-FSCore farm-membership for local player |
| `fscFarmHire` | FSCore: Hire a lounge player. Usage: fscFarmHire <userId/stateId/me> |
| `fscFarmManager` | FSCore: List farm members and roles |
| `fscFarmManagerInit` | FSCore: (Admin only) Set yourself as farm owner |
| `fscFarmProbe` | FSCore: Farm Manager diagnostic dump |
| `fscFarmReconcile` | FSCore: (Admin) Re-sync FSCore roles to vanilla farm membership |
| `fscFarmSet` | FSCore: (Admin) Set a server setting. Usage: fscFarmSet <key> <on/off/number> |
| `fscFarmSettings` | FSCore: List FarmManager server settings + current values |
| `fscFarmTestPlayers` | FSCore: Create demo lounge players for testing |
| `fscFarmUnblock` | FSCore: Unblock a player. Usage: fscFarmUnblock <userId/stateId/me> |

## Farm Manager (phone)

| Command | Description |
|---|---|
| `fscFarmAdmin` | FSCore: Open the Farm Manager panel (members / hire / access rules) |

## Fishing

| Command | Description |
|---|---|
| `fscFish` | Fishing rod status (equip the rod in a utility slot to fish) |
| `fscFishBoardAdmin` | Usage: fscFishBoardAdmin -- open the marina board admin panel (placement / leaderboard / tournaments) |
| `fscFishBoardDisplay` | Usage: fscFishBoardDisplay <y> <z> [rotYdeg] [size] -- position the live text on every board face |
| `fscFishBoardMove` | Usage: fscFishBoardMove -- (multi-board) use the F6 admin panel to select + nudge a board |
| `fscFishBoardPlace` | Usage: fscFishBoardPlace -- ADD a marina bulletin board at your position + heading (multi-board) |
| `fscFishBoardRemove` | Usage: fscFishBoardRemove -- remove ALL marina bulletin boards |
| `fscFishBuyerAdmin` | Usage: fscFishBuyerAdmin -- open the Fish Buyer admin panel (place / wardrobe / prices) |
| `fscFishBuyerMove` | Usage: fscFishBuyerMove -- re-place the Fish Buyer NPC at your current position |
| `fscFishBuyerPlace` | Usage: fscFishBuyerPlace -- place the Fish Buyer NPC at your current position |
| `fscFishBuyerRemove` | Usage: fscFishBuyerRemove -- remove the Fish Buyer NPC |
| `fscFishSellerAdmin` | Usage: fscFishSellerAdmin -- open the Fish Seller admin panel (place / wardrobe / prices) |
| `fscFishSellerMove` | Usage: fscFishSellerMove -- re-place the Fish Seller NPC at your current position |
| `fscFishSellerPlace` | Usage: fscFishSellerPlace -- place the Fish Seller NPC at your current position |
| `fscFishSellerRemove` | Usage: fscFishSellerRemove -- remove the Fish Seller NPC |
| `fscFishSoundTest` | FSCore Fishing: play the mod sounds directly (cast/splash/reel/reel3s/all) |

## Foraging

| Command | Description |
|---|---|
| `fscForageCheck` | FSCore: is this spot mushroom woods? + season status |
| `fscForageHere` | FSCore (admin): grow a mushroom cluster next to you: fscForageHere [chanterelle/porcini/morel] |

## Garage

| Command | Description |
|---|---|
| `fscGarageAddHere` | Place a garage at your current position: fscGarageAddHere [id] |
| `fscGarageAdmin` | Open the Garage admin panel (multi-garage placement + slot-cap settings). |
| `fscGarageList` | List all placed garages. |
| `fscGarageNuke` | Force-remove a stubborn garage entry by tostring-matching its key. Usage: fscGarageNuke <gid-as-displayed> |
| `fscGaragePurgeFlags` | Scrub orphan transient marker flags around a garage. Usage: fscGaragePurgeFlags <gid/all> [radius_m] (default 100m). |
| `fscGarageRemove` | Remove a specific garage: fscGarageRemove <id> |
| `fscGarageRemoveAll` | Remove every placed garage. |

## Identity

| Command | Description |
|---|---|
| `fscCreateIdentity` | FSCore: Force-open the character creation overlay |
| `fscGrantLicense` | FSCore: Admin grant licence. Usage: fscGrantLicense <userId/stateId/me> <licenseId> |
| `fscIdentity` | FSCore: Show your identity card |
| `fscIdentityProbe` | FSCore: Identity diagnostic dump |
| `fscIdentityReset` | FSCore: Reset your identity (debug) |
| `fscLicenses` | FSCore: List your licences |
| `fscRevokeLicense` | FSCore: Admin revoke licence. Usage: fscRevokeLicense <userId/stateId/me> <licenseId> |

## Interaction

| Command | Description |
|---|---|
| `fscInteract` | FSCore: List all registered interaction points |
| `fscInteractNear` | FSCore: Show nearest interaction point and distance |
| `fscInteractProbe` | FSCore: Full diagnostic dump of interaction system state |
| `fscInteractToggle` | FSCore: Toggle an interaction point active/inactive. Usage: fscInteractToggle <pointId> |
| `fscInteractionMode` | FSCore: Get/set selection mode. Usage: fscInteractionMode [auto/proximity/raycast] |

## Inventory

| Command | Description |
|---|---|
| `fscBoostProbe` | Diagnose: prints boost state + local vehicle motor caps |
| `fscClearTrash` | PoC: clear discovery cache (triggers remain registered) |
| `fscFindNode` | PoC: scene-graph search for ANY node containing <substring> |
| `fscInv` | Show your own inventory |
| `fscInvGive` | Give item to yourself: fscInvGive <itemId> [qty] |
| `fscInvGiveTo` | Give item to another player: fscInvGiveTo <userId/stateId/me> <itemId> [qty] |
| `fscInvItems` | List all registered item types |
| `fscInvPlayer` | Show another player's inventory: fscInvPlayer <userId/stateId/me> |
| `fscItemsPath` | Print the modSettings folder + items.xml path for the admin |
| `fscItemsReload` | Re-read modSettings/FSCore/items.xml and re-register every item |
| `fscItemsWriteDefaults` | Overwrite modSettings/FSCore/items.xml with the bundled defaults (LOSES customizations) |
| `fscListTrash` | PoC: print discovered trash/dumpster nodes |
| `fscScanTrash` | PoC: scan map for trash/dumpster nodes + register interaction triggers |

## Inventory (backpack and crates)

| Command | Description |
|---|---|
| `fscClearProps` | Remove all spawned props (optionally filter: fscClearProps [kind]) |
| `fscClothesLockerHere` | Place a clothing locker (change into saved outfits) at your position |
| `fscContainerRecall` | Recall a container pallet to your position: fscContainerRecall [id/label/type] (nearest if omitted) |
| `fscInvBuyFridge` | Buy refrigerator storage at current spot (price 8000, 75kg, 1 per player): fscInvBuyFridge [label] |
| `fscInvBuyShelves` | Buy shelves storage at current spot (price 5000, 100kg, 1 per player): fscInvBuyShelves [label] |
| `fscInvClearPin` | Clear PIN on nearest crate |
| `fscInvContainerNear` | Show nearest container |
| `fscInvContainers` | List all world containers |
| `fscInvSetPin` | Set PIN on nearest crate: fscInvSetPin <pin> |
| `fscInvShare` | Share nearest crate with player: fscInvShare <userId> |
| `fscInvSpawnCrate` | Spawn crate at player position: fscInvSpawnCrate [label] |
| `fscInvUnshare` | Revoke crate access: fscInvUnshare <userId> |
| `fscListProps` | List spawned props with their world positions |
| `fscLockerHere` | Place a locker row at your position |
| `fscLockerList` | List placed locker rows |
| `fscLockerNudge` | Fine-tune a locker: fscLockerNudge <id> <x/y/z/heading> <delta> |
| `fscLockerRemove` | Remove a locker row: fscLockerRemove <id> |
| `fscSpawnPizzaBox` | Spawn a pizza box ~1m in front of you |
| `fscStorageAdmin` | FSCore: Open the storage container (locker) admin panel |

## Lifecycle

| Command | Description |
|---|---|
| `fscLifecycle` | Lifecycle management: fscLifecycle [action] [args] |

## Mini jobs

| Command | Description |
|---|---|
| `fscJobComplete` | Admin complete: fscJobComplete <userId/stateId/me> |
| `fscJobExpire` | Expire a job: fscJobExpire <jobId> |
| `fscJobGenerate` | Force job generation cycle |
| `fscJobLocation` | Manage locations: fscJobLocation add/remove/list/near [name] |
| `fscJobProbe` | Diagnostic dump |
| `fscJobs` | List all jobs on the board |
| `fscJobsPlayer` | Show player job state: fscJobsPlayer <userId/stateId/me> |

## Mini jobs (deliveries and cleanup)

| Command | Description |
|---|---|
| `fscJunkClear` | Clear junk offers: fscJunkClear [offerId/all] |
| `fscJunkList` | List junk offers, claimed piles + settings |
| `fscJunkPay` | Set junk pay: fscJunkPay <itemPay> <bonusPct> |
| `fscJunkSpawn` | Create a junk cleanup offer: fscJunkSpawn [here/zoneName] |
| `fscMiniJobsActive` | Dump active Farm Eats deliveries + dropoff point status |
| `fscMiniJobsAdd` | Add a pickup site of any registered job type at your position:  |
| `fscMiniJobsClearCooldowns` | Clear Farm Eats cooldowns: fscMiniJobsClearCooldowns [all/decline/completion] |
| `fscMiniJobsClearScanLocations` | Wipe scan-added delivery locations (manual entries kept):  |
| `fscMiniJobsDeliveryAdmin` | Open the MiniJobs Delivery admin panel |
| `fscMiniJobsList` | List all pickup sites (id, type, label, position) |
| `fscMiniJobsPurgeOrphans` | Scan for and despawn orphan cargo pallets matching any job-type xml |
| `fscMiniJobsRemove` | Remove a pickup site: fscMiniJobsRemove <id> |
| `fscMiniJobsScanLocations` | Scan map for houses + production points and add as delivery locations:  |
| `fscMiniJobsSweep` | Force a stale-delivery sweep right now: fscMiniJobsSweep [ttlSeconds] |
| `fscMiniJobsTypes` | List registered job types + their cargo/addon config |
| `fscWashClear` | Admin: clear the power-wash board and the washed list |
| `fscWashGrime` | Look test: grime on the washable building nearest you: fscWashGrime <0..1/off> |
| `fscWashList` | List power-wash offers |
| `fscWashOffer` | Admin: put the washable building nearest you on the Giggit board |
| `fscWashScan` | List the washable public buildings, nearest first |

## Needs

| Command | Description |
|---|---|
| `fscNeeds` | Show your current hunger/thirst needs |
| `fscNeedsPlayer` | Show needs for a player: fscNeedsPlayer <userId/stateId/me> |
| `fscNeedsProbe` | Diagnostic: multiplier status, drain tick, all states |
| `fscNeedsRefill` | Refill needs: fscNeedsRefill <userId/stateId/me> |
| `fscNeedsSet` | Set needs: fscNeedsSet <userId/stateId/me> <hunger> <thirst> [fatigue] |
| `fscRestAdd` | Add rest point at player position: fscRestAdd [name] |
| `fscRestList` | List all rest points |
| `fscRestNear` | Find nearest rest point |
| `fscRestRemove` | Remove a custom rest point: fscRestRemove <name> |

## Onboarding

| Command | Description |
|---|---|
| `fscHintsReset` | FSCore: Forget seen lightbulb hints so they fire again. Usage: fscHintsReset [hintId] |
| `fscOnboardingGive` | Force-deliver the starter package to a player |
| `fscOnboardingReset` | Clear a player's starter-package-received flag |
| `fscOnboardingShow` | Print the current starter package contents |

## Farm dogs

| Command | Description |
|---|---|
| `fscPet` | FSCore Pets: status / summon your dog |
| `fscPetBall` | FSCore Pets: drop a fresh ball at you |
| `fscPetBoar` | FSCore Pets: boar-defence status (near-field herds + dog state) |
| `fscPetBonus` | FSCore Pets: set the dog farm-duty animal bonus % (0-100) |
| `fscPetBowl` | FSCore Pets: place / pick up the dog bowl |
| `fscPetBreed` | FSCore Pets: 1 Labrador / 2 Border Collie |
| `fscPetCoat` | FSCore Pets: set coat for current dog type |
| `fscPetDismiss` | FSCore Pets: remove your dog |
| `fscPetMP` | FSCore Pets: print MP diagnostic state (run on client AND server) |
| `fscPetMPSpike` | FSCore Pets: [SERVER] spike-test whether the companion behaves server-side |
| `fscPetNeed` | FSCore Pets: set a need low (hunger/thirst/happy/all) [value] |
| `fscPetPrice` | FSCore Pets: set a Pet Shelter price — fscPetPrice <id> <price> |
| `fscPetPurgeUser` | FSCore Pets: [SERVER] delete a user's pet data — fscPetPurgeUser <uniqueUserId> |
| `fscPetRecover` | FSCore Pets: un-stick a glitched/invisible dog (re-seat + show) |
| `fscPetRide` | FSCore Pets: tune ride offset x y z [headingDeg] |
| `fscPetRideKey` | FSCore Pets: show this vehicle's ride key/offset |
| `fscPetRideSave` | FSCore Pets: save ride offsets to modSettings |
| `fscPetRideScan` | FSCore Pets: preload ride offsets for all shop vehicles (collie default) |
| `fscPetShop` | FSCore Pets: [TEST] grant/reset dog+bed+bowl ownership (arg: reset to lock) |
| `fscPetStoreEdit` | FSCore Pets: open the Pet Shelter seller placement/clothing editor |
| `fscPetStumpProbe` | FSCore Pets: list every tree piece near you and whether the dog counts it as a stump: fscPetStumpProbe [radius] |

## Phone

| Command | Description |
|---|---|
| `fscPhoneApps` | FSCore: List registered phone apps |
| `fscPhoneNotify` | FSCore: Send test notification: fscPhoneNotify [title] [body] |
| `fscPhoneStatus` | FSCore: Show phone core status |

## Placeables and NPCs

| Command | Description |
|---|---|
| `fscNpcEdit` | FSCore: Open NPC editor UI. Usage: fscNpcEdit <name> |
| `fscNpcProbe` | FSCore: Probe GIANTS Engine for NPC/pedestrian spawning APIs |
| `fscOutfit` | FSCore: Change NPC clothing. Usage: fscOutfit <name> <slot> <item> [color] |
| `fscOutfitSlots` | FSCore: List clothing slots/items on NPC. Usage: fscOutfitSlots <name> [slot] |
| `fscPlace` | FSCore: Place object at current position. Usage: fscPlace <type> [name] [degrees] |
| `fscPlaceList` | FSCore: List all placed objects |
| `fscPlaceNear` | FSCore: List placed objects near you. Usage: fscPlaceNear [radius] |
| `fscPlaceProbe` | FSCore: Test which i3d paths load successfully |
| `fscPlaceRegister` | FSCore: Register custom type. Usage: fscPlaceRegister <name> <cat> <path> |
| `fscPlaceTypes` | FSCore: List all available placeable types |
| `fscPoseTest` | FSCore: Test NPC bone rotation. Usage: fscPoseTest <name> <bone> <rx> <ry> <rz> |
| `fscRemove` | FSCore: Remove a placed object. Usage: fscRemove <name> |

## Placement helpers

| Command | Description |
|---|---|
| `fscPlacementNearby` | FSCore: List named nodes near the player, filtered for avatar noise. Optionally tag matches against a pattern. Usage: fscPlacementNearby [radius=5] [pattern] |
| `fscPropCatalog` | FSCore: List every prop key the spawner knows (atm, trashcan, vendingmachine, mailbox, gas tanks, ...) |
| `fscPropClear` | FSCore: Remove every prop you've spawned (does NOT touch map-placed props) |
| `fscPropList` | FSCore: List every prop you've spawned with its id + position |
| `fscPropNear` | FSCore: List spawned props within N meters of the player (default 2m). Usage: fscPropNear [radius] |
| `fscPropPurgeKey` | FSCore: Remove every persisted prop matching a catalog key. One-shot cleanup for orphan kiosk flags. Usage: fscPropPurgeKey <key> |
| `fscPropRemove` | FSCore: Remove a spawned prop. Usage: fscPropRemove <propId> |
| `fscPropSpawn` | FSCore: Spawn a prop at your position. Usage: fscPropSpawn <key>  (see fscPropCatalog) |

## Radial menu

| Command | Description |
|---|---|
| `fscRadial` | FSCore: open the radial menu |
| `fscRadialDump` | FSCore: list registered radial categories |

## Reputation

| Command | Description |
|---|---|
| `fscRep` | FSCore: Show your reputation levels |
| `fscRepGive` | FSCore: Admin grant XP. Usage: fscRepGive <userId/stateId/me> <skill> <amount> |
| `fscRepLeaderboard` | FSCore: Show top 10 for a skill. Usage: fscRepLeaderboard <skill> |
| `fscRepPlayer` | FSCore: Show reputation for a player. Usage: fscRepPlayer <userId/stateId/me> |
| `fscRepProbe` | FSCore: Reputation diagnostic dump |
| `fscRepReset` | FSCore: Admin reset player reputation. Usage: fscRepReset <userId/stateId/me> |

## Salvaging

| Command | Description |
|---|---|
| `fscSalvageBuyerAdmin` | Usage: fscSalvageBuyerAdmin -- open the Salvage Buyer admin panel (place / wardrobe / prices) |
| `fscSalvageBuyerMove` | Usage: fscSalvageBuyerMove -- re-place the Salvage Buyer NPC at your current position |
| `fscSalvageBuyerPlace` | Usage: fscSalvageBuyerPlace -- place the Salvage Buyer NPC at your current position |
| `fscSalvageBuyerRemove` | Usage: fscSalvageBuyerRemove -- remove the Salvage Buyer NPC |
| `fscSalvagingClearCooldowns` | Admin: clear every container's cooldown |
| `fscSalvagingConfigPath` | Print the modSettings paths the config loader uses |
| `fscSalvagingCount` | Print discovered + cooldown counts |
| `fscSalvagingList` | List discovered containers with world positions |
| `fscSalvagingNearby` | List named nodes near the player. Usage: fscSalvagingNearby [radius=5] |
| `fscSalvagingReloadConfig` | Re-read modSettings/FSCore/salvaging.xml + re-register items |
| `fscSalvagingRoll` | Diagnostic: print one loot roll without delivering |
| `fscSalvagingScan` | Scan map for trash / salvaging / debris containers |
| `fscSalvagingStatus` | Print which inventory + economy providers we resolved |

## Scavenger

| Command | Description |
|---|---|
| `fscScavengerAdmin` | FSCore: Toggle the Scavenger admin control panel |
| `fscScavengerHide` | FSCore: Hide every active spawn from the PDA map |
| `fscScavengerPlaceCollector` | FSCore: Place the collector NPC at your feet, facing your direction |
| `fscScavengerRemoveCollector` | FSCore: Remove the collector NPC |
| `fscScavengerReset` | FSCore: Reset — same as Stop today; will also wipe per-player collected counts once persistence ships |
| `fscScavengerReveal` | FSCore: Reveal every active spawn on the PDA map |
| `fscScavengerScan` | FSCore: Drop PDA preview hotspots on N legal spawn points (NO spawn). Usage: fscScavengerScan <count> |
| `fscScavengerScanClear` | FSCore: Clear all scan-preview hotspots |
| `fscScavengerSpawnOne` | FSCore: Spawn one item at your feet (pickup test). Usage: fscScavengerSpawnOne [typeId] |
| `fscScavengerStart` | FSCore: Start a scavenger event. Usage: fscScavengerStart [typeId] [count] |
| `fscScavengerStatus` | FSCore: Scavenger status |
| `fscScavengerStop` | FSCore: Stop the active event (despawns remaining items + hotspots) |
| `fscScavengerThumbBooth` | FSCore: Thumbnail photo booth — cycles every item in front of the camera. Usage: fscScavengerThumbBooth [intervalSec] |

## Services (UI)

| Command | Description |
|---|---|
| `fscServicesRemoveByLabel` | FSCore: Remove EVERY store location whose label matches the argument. Usage: fscServicesRemoveByLabel Cooler |
| `fscServicesVendingList` | FSCore: List every node the vending scanner has matched, with its name + position |
| `fscServicesVendingReset` | FSCore: Remove all scanner-registered vending/cooler locations and clear the scanner cache (use to retune patterns) |
| `fscServicesVendingScan` | FSCore: Scan the map for vending machines / coolers and auto-register each as a general store |
| `fscVendingHideNear` | FSCore: Hide the vending machine nearest you (decor / unreachable) - never registered again, saved with the map layout. Usage: fscVendingHideNear [radiusM=25] |
| `fscVendingUnhideAll` | FSCore: Bring back every hidden vending machine (they register on the next scan / restart) |

## SimpliBarn (barn cameras)

| Command | Description |
|---|---|
| `fscSimpliBarnTest` | SimpliBarn: send a test intrusion alert. Usage: fscSimpliBarnTest [zoneId] |

## Sitting and emotes

| Command | Description |
|---|---|
| `fscEmote` | FSCore: play an emote. Usage: fscEmote <wave/crossed/hips/shrug/think/salute/clap/lean/stop> |
| `fscSitHeight` | FSCore: tune the seated height. Usage: fscSitHeight <metres> |

## Chat commands

| Command | Description |
|---|---|
| `fscSlash` | FSCore: SlashCommand diagnostic. Usage: fscSlash [list/status] |

## Theme

| Command | Description |
|---|---|
| `fscTheme` | FSCore Theme — show/list/set/contexts/probe |

## UI

| Command | Description |
|---|---|
| `fscIcon` | FSCore: Icon/Hotspot tools. Usage: fscIcon <test/testall/remove/list/icons/probe> |
| `fscIconsPath` | FSCore: Print the modSettings folder path where admin icon files belong. |
| `fscIconsReload` | FSCore: Invalidate the item-icon cache so re-resolution picks up newly-added DDS files in modSettings/FSCore/img/items/ |
| `fscIconsReseed` | FSCore: Re-copy bundled item icons into modSettings/FSCore/img/items/. Optional arg 'force' overwrites admin edits. |
| `fscMoneyHudReset` | FSCore: Panic-clear every active money-HUD suppressor (use if an admin UI crashed mid-open and the wallet HUD is stuck off). |

## Utilities

| Command | Description |
|---|---|
| `fscLogLevel` | Show or set the FSCore log level (error/warn/info/debug) |
| `fscProfile` | FSCore: time every module's update() and name the ones that hitch (fscProfile [ms] / off) |

## Vehicle keys and licenses

| Command | Description |
|---|---|
| `fscLicense` | FSCore: Admin licence. Usage: fscLicense <userId/stateId/me> grant/revoke/show <car/tractor/heavy/licenseId> |
| `fscLicenseClass` | FSCore: Which licence the vehicle you're in (or nearest) needs, and why |
| `fscLicenseReload` | FSCore: Admin re-read modSettings/FS25_FSCore/licenses.xml and push it to all clients |
| `fscVehicleKey` | FSCore: Give spare key. Usage: fscVehicleKey <stateId> |
| `fscVehicleKeyRevoke` | FSCore: Revoke spare key. Usage: fscVehicleKeyRevoke <stateId> |
| `fscVehicleKeys` | FSCore: List your locked vehicles and keys |
| `fscVehicleLock` | FSCore: Lock the vehicle you're in |
| `fscVehicleProbe` | FSCore: Vehicle diagnostic dump |
| `fscVehicleUnlock` | FSCore: Unlock the vehicle you're in |

## Vehicle rentals

| Command | Description |
|---|---|
| `fscRentalAdmin` | Open the Vehicle Rentals admin panel (kiosk placement + per-vehicle pricing). |
| `fscRentalCatalogList` | Print every catalog entry currently loaded (key, price, deposit, availability). |
| `fscRentalCatalogReload` | Re-read modSettings/FSCore/rental_catalog.xml and re-register every rental vehicle. |
| `fscRentalCatalogWriteDefaults` | Overwrite modSettings/FSCore/rental_catalog.xml with the bundled defaults (LOSES customizations). |
| `fscRentalKioskHere` | Place the APE Rentals kiosk at your current position. |
| `fscRentalKioskRemove` | Remove the rental kiosk (despawns NPC, interaction, hotspot). |
| `fscRentalPurgeFlags` | Scrub orphan transient marker flags around the kiosk. Usage: fscRentalPurgeFlags [radius_m] (default 100m). |
| `fscRentalPurgeOrphans` | Scan for and despawn orphan rental vehicles near the kiosk (server-only). |
| `fscRentalReturn` | Force-return a rental: fscRentalReturn <userId/me> |
| `fscRentalStatus` | Show all active rentals. |
| `fscRentalSweep` | Force a stale-rental sweep right now (server-only, no deposit refund). |

## Vehicles

| Command | Description |
|---|---|
| `fscVehicle` | Vehicle management: fscVehicle <action> [args] |

## Welcome boards

| Command | Description |
|---|---|
| `fscWelcome` | Welcome board: fscWelcome list/inspect <articleId> |
| `fscWelcomeAdd` | Add article: fscWelcomeAdd <category> <title> |
| `fscWelcomeBoard` | Board mgmt: fscWelcomeBoard add/remove/list/near [name] |
| `fscWelcomeDelete` | Delete article: fscWelcomeDelete <articleId> |
| `fscWelcomeGift` | Show gift config |
| `fscWelcomePin` | Toggle pin: fscWelcomePin <articleId> |
| `fscWelcomeProbe` | Diagnostic dump |
| `fscWelcomeResetClaim` | Reset claim: fscWelcomeResetClaim <userId/stateId/me> |
| `fscWelcomeResetSeen` | Reset seen: fscWelcomeResetSeen <userId/stateId/me> |
| `fscWelcomeSetArticle` | Set welcome article: fscWelcomeSetArticle <articleId> |
| `fscWelcomeSetGift` | Set gift: fscWelcomeSetGift <itemId> <qty> [<itemId> <qty> ...] |

## Welcome boards (UI)

| Command | Description |
|---|---|
| `fscWelcomeSignAdmin` | Open the Welcome Signs admin panel (spawn / rename / move signs). |

## World

| Command | Description |
|---|---|
| `fscBoar` | Wild boar: fscBoar — list detected boar herds + whether on your land |
| `fscLand` | Land ownership: fscLand [farmId] — owned parcels + fields |
| `fscSpeedZone` | Speed zones: fscSpeedZone add/remove/list/probe [args] |
| `fscWorld` | World state: fscWorld [domain] |
| `fscWorldAnimals` | Animal/husbandry summary |
| `fscWorldPlayers` | Connected player summary |
| `fscWorldProbe` | Diagnostic dump |
| `fscWorldTime` | Current time state |
| `fscWorldVehicles` | Vehicle summary |
| `fscWorldWeather` | Current weather state |
