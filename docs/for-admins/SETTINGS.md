# Server Settings Reference

Every rule on the **FSCore Settings** page (pause menu, **FSCore** tab), in the order and tabs the page shows them. An administrator changes any rule live; the choice is saved with the savegame and sent to every connected player. Other players see the page read-only. Rules marked *multiplayer only* have no effect in singleplayer.

FSCore 1.0.0.0: **93 settings** on 6 tabs, among them **50 module switches** on the FEATURES tab. The PLAYERS tab is not a rule list: it is where an administrator looks up a player and resets their character, licences or skills. The rule id in the last column is the name other mods read through `g_currentMission.FSCore.Config`.

Community-project rules (shift length, waits, Town Hall pay, crane limits) are not on this page: they are set in **Admin Hub (F6) > Community Projects > RULES**. See [COMMUNITY_PROJECTS.md](COMMUNITY_PROJECTS.md).

*This page is generated from the FSCore 1.0.0.0 source. Default = what a brand-new savegame starts with; a saved choice always wins.*

## Tabs

- [FEATURES](#features) (50)
- [MOVEMENT](#movement) (7)
- [VEHICLES](#vehicles) (7)
- [ECONOMY](#economy) (14)
- [WORLD](#world) (9)
- [INTERFACE](#interface) (6)

## FEATURES

| Setting | What it does | Default | Choices | Rule id |
|---|---|---|---|---|
| Module: Boating | Rent boats at the marina and cruise, anchor and fish from the deck. | **ON** | on / off | `enable_boating` |
| Module: F9 Radial Menu | The F9 radial menu with dog commands, emotes and quick actions. Off: those quick actions are not available (the admin hub keeps its own key). | **ON** | on / off | `enable_radial` |
| Module: Backpack & Items | The F10 backpack, carried items and dropped items. Fishing, Salvaging, Scavenger, Crafting, Storage Lockers, Shops, Pets and Survival Needs need it: switching it off turns them off too. | **ON** | on / off | `enable_inventory` |
| Module: Bulletin Board | Community bulletin boards and the Bulletin phone app: posts, notices and listings. | **ON** | on / off | `enable_bulletin` |
| Module: Cash & ATMs | Pocket cash and the ATMs that move it to and from the bank. Off: there is no pocket cash - every payment goes straight to and from the bank account. | **ON** | on / off | `enable_cash` |
| Module: Character & ID Card | The character creator on first join and the ID card. Off: players play under their game name. Equipment Licences need it. | **ON** | on / off | `enable_identity` |
| Module: Chat Commands | The / commands in chat (for example /needs). | **ON** | on / off | `enable_slashcommands` |
| Module: Clothing System | Outfit store, wardrobe and clothing pricing. | **ON** | on / off | `enable_clothing` |
| Module: Compass | A compass heading at the top of the player HUD. | **ON** | on / off | `compass_enabled` |
| Module: Crafting | Workbench recipes and the Crafting phone app. Off: the workbenches are not placed. | **ON** | on / off | `enable_crafting` |
| Module: Dealership | Vehicle dealership with financing and ownership records. Garage and Marketplace need it: switching Dealership off turns them off too. Off: vehicle loans are paused until it is back on. | **ON** | on / off | `enable_dealership` |
| Module: Employment | Farm jobs with a clock-in kiosk and payroll. | **ON** | on / off | `enable_employment` |
| Module: Farm Garage | Park, store and spawn farm vehicles from a garage. | **ON** | on / off | `enable_farmgarage` |
| Module: Farm Roles | Farm Manager roles and permissions, hiring and applications. Off: the game's own farm management. | **ON** | on / off | `enable_farmroles` |
| Module: Fishing | Rods, bait, fish buyers, marina boards and tournaments. Also switches mushrooms, the camp chair and the fire pit. | **ON** | on / off | `enable_fishing` |
| Module: Fuel Stations | FSCore fuel pumps with nozzle refuelling, fuel prices and farm fuel tanks. Off: the game's own refuelling. | **ON** | on / off | `enable_fuel` |
| Module: Garage | Personal vehicle garage storage and transfers. Needs the Dealership module: with Dealership off, Garage stays off too. | **ON** | on / off | `enable_garage` |
| Module: Equipment Licences | Vehicles need a licence by class: cars for everyone, an Ag Operator licence for tractors, harvesters and other farm machines, a Truck Licence for road trucks and semis, a Forestry licence for forestry machines. Players apply in the phone ID card app (reputation + fee). Class map: modSettings/FSCore/licenses.xml. Admins bypass in multiplayer. | OFF | on / off | `enable_licenses` |
| Module: Marketplace | Players sell and rent vehicles to each other. Needs the Dealership module. | **ON** | on / off | `enable_marketplace` |
| Module: Map Essentials | Vending machines, trash bins, dumpsters and decorations placed across the map. Workbenches follow Crafting, street-light decorations Seasonal Street Lights. | **ON** | on / off | `enable_essentials` |
| Module: MiniJobs | Giggit gigs: parcel deliveries, junk cleanup and the delivery tables. | **ON** | on / off | `enable_minijobs` |
| Module: Shiftit | Shiftit company shifts: mail, parcels, propane, towing and refuse rounds in company vehicles from the Shiftit yard, and the Shiftit app. Needs MiniJobs. Off: no yard, no shifts and no app; careers stay saved. | **ON** | on / off | `enable_shiftit` |
| Module: Lawn Care | Lizard Lawncare mowing contracts in Shiftit: roadside stretches, homes for sale and public grass, with the ZT 60 and UT 80 trailer for starters and a Deutz-Fahr 6C with Samasz mowers from rank 3. Mowing is allowed in the job's area while the shift runs. Needs Shiftit. Off: no mowing jobs and the company is hidden; careers stay saved. | **ON** | on / off | `enable_lawncare` |
| Module: Pets | Farm dogs with needs, beds, bowls and farm duty (the animal production bonus). | **ON** | on / off | `enable_pets` |
| Module: Farm Storage Barn | With Central Farm Storage - Pallets installed, the Farm Storage Barn collects: once every in-game hour the full pallets at the farm's own barns (eggs, wool, goat milk), beehives (honey) and productions set to store (bottled milk, greenhouse produce...) within 150 m go into the farm's storage barn. Off: the barns are storage you fill by hand; nothing is lost. | **ON** | on / off | `enable_farmstore` |
| Module: Milk House | With Central Farm Storage - Milk House installed, the Milk House collects: once every in-game hour the cow milk and buffalo milk in the farm's own barns within 150 m goes into the matching tank of the nearest milk house, up to its free capacity. Off: the milk houses are tanks you fill by trailer; nothing is lost. | **ON** | on / off | `enable_milkhouse` |
| Module: Farming | Counts the farm work each player does by hand or with their AI helpers: harvesting, mowing, tedding, raking, baling, wrapping, sowing, cultivating, ploughing, spraying, feeding and bedding animals, felling trees and contracts. Earns Farm Points, the 15 farming ranks (shown under name tags), medals with a little skill XP, a Farmer of the Week and Farming Report posts on Farm Feed. Shown in the Farming app. Off: nothing is counted; the counts stay saved. | **ON** | on / off | `enable_farming` |
| Module: Phone | The smartphone (/ key): messages, contacts, bank, weather, notifications and every module app. Off: notices show as in-game messages, and the phone-only features (Giggit, Farm Eats, Finance, Journey, dog adoption, SimpliBarn) are not available. | **ON** | on / off | `enable_phone` |
| Module: PlotView & HerdSync | Field information and herd overview apps on the phone. | **ON** | on / off | `enable_plotview` |
| Module: Reputation & XP | Community XP, levels and titles. Off: nothing is locked behind a level. | **ON** | on / off | `enable_reputation` |
| Module: Real Estate | The map's houses as homes to buy from Lizard Realty (outright or with a mortgage), with interiors, a FOR SALE sign, a home garage, the plot and spare keys. Admins set the homes up. Needs the Phone module (Real Estate app). Off: nothing is shown and mortgage payments pause; the homes stay saved. | **ON** | on / off | `enable_realestate` |
| Module: Construction | Building from a plan: set out a site, bring the pallets, build it up stage by stage with a hammer and trowel. Garden sheds and raised beds; building materials and pallet orders at the general store's supply yard. Needs the Backpack. Off: building sites are not shown and nothing can be built; they stay saved. | **ON** | on / off | `enable_construction` |
| Module: Raised Bed Garden | Raised beds that grow crops through the seasons: soil, seeds, the watering can, fertiliser and the harvest. Needs Construction (the beds are built from plans). Off: nothing grows and the beds' crops are not shown; they stay saved. | **ON** | on / off | `enable_garden` |
| Module: Salvaging | Find, collect and sell salvage to the salvage buyer. | **ON** | on / off | `enable_salvaging` |
| Module: Mining | The underground mine: an entrance with a lift, a maze dug a section at a time, ore veins, pickaxes and the rock drill, headlamps, finds, track and ore carts, the mine forge, the Mining skill and the Mine app. Needs the Backpack. Off: the entrance is not placed and nothing below runs; the dig stays saved. | **ON** | on / off | `enable_mining` |
| Module: Road Names & GPS | The map's roads get street names: homes and letterboxes get addresses on them, the street you drive on shows under the compass, with turn-by-turn directions and the phone's Navigation app. Off: addresses use area street names and there is no GPS. | **ON** | on / off | `enable_roads` |
| Module: Scavenger | Search bins and spots for collectibles to sell. | **ON** | on / off | `enable_scavenger` |
| Module: Seasonal Street Lights | Map Essentials > SEASONAL: lit decorations on the map's street lights, by theme or by calendar. | **ON** | on / off | `enable_seasonal` |
| Module: Shops | FSCore shop counters: the general store and food shops. Needs Backpack & Items. | **ON** | on / off | `enable_shops` |
| Module: Silo Product List | A sorted product list with fill bars at silos and loading stations. Off: the game's own silo dialog. | **ON** | on / off | `enable_silo` |
| Module: Sit & Emotes | Sit on benches and chairs, and emotes from the F9 radial menu. | **ON** | on / off | `enable_sit` |
| Module: Storage Lockers & Fridge | Placed storage lockers and each farm's shared fridge. Off: they are not placed; what is stored in them stays saved. | **ON** | on / off | `enable_lockers` |
| Module: Survival Needs | Hunger, thirst and fatigue, what food and drink do, and the needs dials. | **ON** | on / off | `enable_needs` |
| Module: Taxes & Invoices | Income tax, VAT, property tax and invoices between players and farms. Off: no FSCore taxes or invoices; bank and loans stay. | **ON** | on / off | `enable_taxes` |
| Module: Vehicle Rentals | Rent vehicles from a catalogue with deposits and returns. | **ON** | on / off | `enable_vehiclerentals` |
| Module: Vehicle Keys | Vehicle locks and keys for personal and farm vehicles. Off: vehicles are never locked. | **ON** | on / off | `enable_vehiclekeys` |
| Module: Welcome Boards | Welcome boards with the welcome gift, Town Hall news and the Town Hall phone app. | **ON** | on / off | `enable_welcomeboard` |
| Module: Journey | The first-day checklist on the phone: short steps that teach FSCore by doing, each paying a small welcome grant and Community XP. Experienced players can skip it. | **ON** | on / off | `enable_journey` |
| Module: Lightbulb Hints | One-time tips on the phone the first time a player walks up to a kiosk, a job board or a new feature. Each player can also switch them off in the phone's Settings app. | **ON** | on / off | `enable_hints` |
| Module: Feed Ratio Lock | Pigs and horses eat all their foods at once. Each food gets its own share of the trough, sized to how much of it the animals really eat, so one crop can no longer fill the whole trough. | **ON** | on / off | `enable_feed_ratio` |

## MOVEMENT

| Setting | What it does | Default | Choices | Rule id |
|---|---|---|---|---|
| Disable 'Tab' Switching | Forces players to physically walk to their vehicles. | OFF | on / off | `disable_tab_switch` |
| Disable Map Teleporting | Removes the ability to click the in-game map to fast-travel. | OFF | on / off | `disable_map_teleport` |
| Block gsTeleport Console Command | Intercepts and blocks the teleport cheat, even for admins. | OFF | on / off | `disable_teleport_cheat` |
| Disable Flight Mode | Blocks players from enabling the 'J' debug flight mode. | OFF | on / off | `disable_flight` |
| Block Super Strength | Prevents the use of the developer super strength cheat. | OFF | on / off | `disable_super_strength` |
| Lock To Arrivals Lounge Until Hired | MULTIPLAYER ONLY. Players without a farm assignment from a prior session always land on the Arrivals Lounge farm. ON: non-admin players also cannot switch farms from the Multiplayer Overview screen until a farm owner or manager hires them through the Farm Manager app. Has no effect in singleplayer. | **ON** | on / off | `force_arrivals_lounge` |
| Save Disconnect Location | Players spawn exactly where they logged off. | **ON** | on / off | `persist_exit_position` |

## VEHICLES

| Setting | What it does | Default | Choices | Rule id |
|---|---|---|---|---|
| Require Manual Implement Attach | Players must stand on foot near the hitch to connect equipment. | OFF | on / off | `manual_attach` |
| Disable AI Workers | Globally blocks the 'Hire Worker' action. | OFF | on / off | `disable_ai_workers` |
| Block Ignition on Written-Off Vehicles | Engines will not start once damage reaches 100%. | **ON** | on / off | `dead_at_damage` |
| Fatigue Affects Vehicle Power | Dynamically reduces engine torque when the driver's fatigue is high. | OFF | on / off | `vehicle_fatigue_penalty` |
| Realistic Refuelling (Hand Nozzle) | Disables in-vehicle refuelling at fuel triggers. Get out, press R at a pump or fuel tank to take the nozzle, and aim it at the vehicle to fuel. | OFF | on / off | `nozzle_fueling` |
| Split Fuel Billing | Fuel for farm machinery is charged to the vehicle's farm account. Personal road vehicles pay from the driver's cash, and farm-fuel locations refuse them (dyed diesel). | OFF | on / off | `farm_fuel_billing` |
| Market-Based Fuel Pricing | Public station prices track the game's live diesel price times the selected retail markup, moving with difficulty and market swings. Stations with an admin-set price keep it. | **Discount (0.7x)** | Discount (0.7x) / Reduced (0.85x) / At Cost (1.0x) / Low Markup (1.1x) / Retail (1.2x) / Premium (1.35x) / Peak Markup (1.5x) | `dynamic_fuel_pricing` |

## ECONOMY

| Setting | What it does | Default | Choices | Rule id |
|---|---|---|---|---|
| Override Starting Funds | Sets the exact bank balance for new players joining the server. | **100,000** | 10,000 / 50,000 / 100,000 / 250,000 / 1,000,000 / 5,000,000 | `starting_cash` |
| Auto-Deliver Starter Package On First Spawn *(multiplayer only)* | MULTIPLAYER ONLY. ON: new players receive the configured Welcome Package automatically the first time they spawn in - no Welcome Board visit required. OFF: players must walk up to a Welcome Board and click Claim Gift to receive their package. Package contents are defined in modSettings/FSCore/welcomePackage.xml. In singleplayer the package is always auto-delivered on first spawn regardless of this setting. | OFF | on / off | `auto_deliver_starter` |
| Show Welcome Board To New Players *(multiplayer only)* | MULTIPLAYER ONLY. ON: a player who has not seen the welcome post yet gets the Welcome Board on screen after the Arrivals screen and character creation, with the welcome post open. OFF: players only see it when they walk up to a Welcome Board. Has no effect in singleplayer. | **ON** | on / off | `auto_open_welcome` |
| Lock the shop (P menu) - buying | Players cannot buy through the game's shop. Servers that route purchases through the FSCore dealership turn this on. | OFF | on / off | `disable_menu_shopping` |
| Lock the shop (P menu) - selling | Players cannot sell through the game's shop. Servers that route sales through the FSCore dealership turn this on. | OFF | on / off | `disable_menu_selling` |
| Trade-In Value | Shop sell price as a percent of the vanilla figure. Business reputation adds +1% per level and a machine under 10% damage adds +5%; the total is capped at 150%. | **100%** | 50% / 75% / 100% / 125% / 150% | `trade_in_value_pct` |
| Require Livestock Trailers | Disables direct-to-pasture teleportation from the animal dealer. | OFF | on / off | `animals_require_trailer` |
| Disable Map Land Purchases | Players must use the real-estate point in the world instead. | OFF | on / off | `disable_field_buying` |
| 50% Land Resale Penalty | Halves the refund for sold farmland. | OFF | on / off | `anti_flip_farmland` |
| Disable Bank Loans | Sets the vanilla borrowing limit to zero. | OFF | on / off | `disable_loans` |
| Disable NPC Contracts | Stops the game generating random field contracts. | OFF | on / off | `disable_npc_contracts` |
| Disable Contract Equipment Borrowing | Forces players to use their own machinery for NPC contracts. | OFF | on / off | `contracts_no_lease` |
| Lock Factory Output to 'Storing' | Prevents players from auto-selling or distributing production goods. | OFF | on / off | `production_storage_only` |
| Block gsMoneyAdd Console Command | Intercepts and blocks the money cheat, even for admins. | OFF | on / off | `disable_money_cheat` |

## WORLD

| Setting | What it does | Default | Choices | Rule id |
|---|---|---|---|---|
| Lock Time Scale | Forces a constant server time speed, overriding manual changes. | **Off (players choose)** | Off (players choose) / 1x (real-time) / 5x / 30x / 60x / 120x / 1000x | `lock_timescale` |
| Auto-Skip Night-time | Speeds up time during the configured night hours. | **Aggressive (18:00->06:00 @ 1000x)** | Off / Mild (18:00->06:00 @ 30x) / Standard (18:00->06:00 @ 60x) / Fast (18:00->06:00 @ 120x) / Aggressive (18:00->06:00 @ 1000x) | `fast_forward_night` |
| Disable Sleep Triggers | Blocks players from using farmhouse beds to skip time. | **ON** | on / off | `disable_sleep` |
| Require Fishing Licence | Players must hold a Fishing licence (sold at the general store, or granted in Settings) before they can cast. | **ON** | on / off | `require_fishing_license` |
| Disable Rain Harvest Penalty | Removes the vanilla yield reduction when harvesting in storms. | **ON** | on / off | `harvest_in_rain` |
| Remove Map NPCs | Removes the decorative pedestrians walking around the map. | OFF | on / off | `remove_npcs` |
| Eat / Drink Time | How long the hold-to-consume meter takes when eating food or drinking (seconds). Applies to all players. | **Default (5s)** | Fast (3s) / Default (5s) / Relaxed (10s) / Standard (15s) / Slow (25s) / Realistic (45s) | `consume_duration` |
| Trim Overfilled Troughs | Troughs holding more of a food than its share are cut back to the share when the savegame loads and when this is switched on. The extra food is removed and not refunded. | OFF | on / off | `feed_ratio_trim` |
| Farm Fridge Size | Slots in each farm's shared fridge. Every member can stock it and take from it; only food, drink and dog food fit, and food in it goes stale at half speed. | **Standard (12 slots)** | Small (8 slots) / Standard (12 slots) / Large (16 slots) / Extra Large (20 slots) / Walk-in (24 slots) | `farm_fridge_slots` |

## INTERFACE

| Setting | What it does | Default | Choices | Rule id |
|---|---|---|---|---|
| Hide Vanilla Money HUD | Removes the cash balance from the top right corner. | OFF | on / off | `hide_money_hud` |
| Hide Player Nametags *(multiplayer only)* | Removes floating names for better immersion. | **ON** | on / off | `disable_nametags` |
| Teardrop Kiosk Flags | Bright teardrop banners with a symbol and a word at every NPC kiosk. Off: the classic hanging flags. Applies to flags placed after the change (a restart refreshes all). | **ON** | on / off | `teardrop_flags` |
| Chat Text Scale | Adjusts the size of the multiplayer chat box. | **Large (130%)** | Vanilla (100%) / Large (130%) / Huge (175%) / Max (200%) | `chat_size_scale` |
| Chat Fade Delay | Controls how long messages stay visible before fading out. | **Extended (25s)** | Vanilla (10s) / Extended (25s) / Long (45s) / Persistent (90s) | `chat_visible_duration` |
| Auto-Skip Guided Tour | Skips the singleplayer tutorial prompts when the map loads. | **ON** | on / off | `disable_guided_tour` |

