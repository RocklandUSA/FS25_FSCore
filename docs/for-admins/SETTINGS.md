# Server Settings Reference

Every rule on the **FSCore Settings** page (pause menu, FSCore tab), grouped the way the page groups them. An administrator flips any rule live; the state is saved with the game and sent to every connected player. Rules marked *multiplayer only* have no effect in singleplayer.

Total: **63 rules**.

## ECONOMY

| Rule | What it does | Default | Choices |
|---|---|---|---|
| Override Starting Funds | Sets the exact bank balance for new players joining the server. | **ON** (100000) | 10,000 / 50,000 / 100,000 / 250,000 / 1,000,000 / 5,000,000 |
| Auto-Deliver Starter Package On First Spawn *(multiplayer only)* | MULTIPLAYER ONLY. ON: new players receive the configured Welcome Package automatically the first time they spawn in - no Welcome Board visit required. OFF: players must walk up to a Welcome Board and click Claim Gift to receive their package. Package contents are defined in modSettings/FSCore/welcomePackage.xml. In singleplayer the package is always auto-delivered on first spawn regardless of this setting. | OFF | on / off |
| Show Welcome Board To New Players *(multiplayer only)* | MULTIPLAYER ONLY. ON: a player who has not seen the welcome post yet gets the Welcome Board on screen after the Arrivals screen and character creation, with the welcome post open. OFF: players only see it when they walk up to a Welcome Board. Has no effect in singleplayer. | **ON** | on / off |
| Lock the shop (P menu) - buying | Players cannot buy through the game's shop. Servers that route purchases through the FSCore dealership turn this on. | OFF | on / off |
| Lock the shop (P menu) - selling | Players cannot sell through the game's shop. Servers that route sales through the FSCore dealership turn this on. | OFF | on / off |
| Trade-In Value | Shop sell price as a percent of the vanilla figure. Business reputation adds +1% per level and a machine under 10% damage adds +5%; the total is capped at 150%. | **ON** (100) | 50% / 75% / 100% / 125% / 150% |
| Require Livestock Trailers | Disables direct-to-pasture teleportation from the animal dealer. | OFF | on / off |
| Disable Map Land Purchases | Players must use the real-estate point in the world instead. | OFF | on / off |
| 50% Land Resale Penalty | Halves the refund for sold farmland. | OFF | on / off |
| Disable Bank Loans | Sets the vanilla borrowing limit to zero. | OFF | on / off |
| Disable NPC Contracts | Stops the game generating random field contracts. | OFF | on / off |
| Disable Contract Equipment Borrowing | Forces players to use their own machinery for NPC contracts. | OFF | on / off |
| Lock Factory Output to 'Storing' | Prevents players from auto-selling or distributing production goods. | OFF | on / off |
| Block gsMoneyAdd Console Command | Intercepts and blocks the money cheat, even for admins. | OFF | on / off |

## MODULES

| Rule | What it does | Default | Choices |
|---|---|---|---|
| Module: Boating | Rent boats at the marina and cruise, anchor and fish from the deck. | **ON** | on / off |
| Module: Clothing System | Outfit store, wardrobe and clothing pricing. | **ON** | on / off |
| Module: Dealership | Vehicle dealership with financing and ownership records. The Garage module needs it: switching Dealership off also turns Garage off. | **ON** | on / off |
| Module: Farm Garage | Park, store and spawn farm vehicles from a garage. | **ON** | on / off |
| Module: Fishing | Rods, bait, fish buyers, marina boards and tournaments. | **ON** | on / off |
| Module: Garage | Personal vehicle garage storage and transfers. Needs the Dealership module: with Dealership off, Garage stays off too. | **ON** | on / off |
| Module: Equipment Licences | Vehicles need a licence by class: cars for everyone, a Tractor Licence for everyday farm machines, a Heavy Equipment Licence for trucks, harvesters, forestry machines and anything over 300 hp or 12 t. Players apply in the phone ID card app (reputation + fee). Class map: modSettings/FS25_FSCore/licenses.xml. Admins bypass in multiplayer. | OFF | on / off |
| Module: MiniJobs | Giggit gigs: parcel deliveries, junk cleanup and the delivery tables. | **ON** | on / off |
| Module: Pets | Farm dogs with needs, beds, bowls and farm duty. | **ON** | on / off |
| Module: Phone | The smartphone (/ key): messages, contacts, bank, weather, notifications and every module app. | **ON** | on / off |
| Module: Salvaging | Find, collect and sell salvage to the salvage buyer. | **ON** | on / off |
| Module: Scavenger | Search bins and spots for collectibles to sell. | **ON** | on / off |
| Module: Vehicle Rentals | Rent vehicles from a catalogue with deposits and returns. | **ON** | on / off |
| Module: Journey | The first-day checklist on the phone: short steps that teach FSCore by doing, each paying a small welcome grant and Community XP. Experienced players can skip it. | **ON** | on / off |
| Module: Lightbulb Hints | One-time tips on the phone the first time a player walks up to a kiosk, a job board or a new feature. Each player can also switch them off in the phone's Settings app. | **ON** | on / off |
| Module: Feed Ratio Lock | Pigs and horses eat all their foods at once. Each food gets its own share of the trough, sized to how much of it the animals really eat, so one crop can no longer fill the whole trough. | **ON** | on / off |

## MOVEMENT

| Rule | What it does | Default | Choices |
|---|---|---|---|
| Disable 'Tab' Switching | Forces players to physically walk to their vehicles. | OFF | on / off |
| Disable Map Teleporting | Removes the ability to click the in-game map to fast-travel. | OFF | on / off |
| Block gsTeleport Console Command | Intercepts and blocks the teleport cheat, even for admins. | OFF | on / off |
| Disable Flight Mode | Blocks players from enabling the 'J' debug flight mode. | OFF | on / off |
| Block Super Strength | Prevents the use of the developer super strength cheat. | OFF | on / off |
| Lock To Arrivals Lounge Until Hired | MULTIPLAYER ONLY. Players without a farm assignment from a prior session always land on the Arrivals Lounge farm. ON: non-admin players also cannot switch farms from the Multiplayer Overview screen until a farm owner or manager hires them through the Farm Manager app. Has no effect in singleplayer. | **ON** | on / off |
| Save Disconnect Location | Players spawn exactly where they logged off. | **ON** | on / off |

## UI

| Rule | What it does | Default | Choices |
|---|---|---|---|
| Hide Vanilla Money HUD | Removes the cash balance from the top right corner. | OFF | on / off |
| Hide Player Nametags *(multiplayer only)* | Removes floating names for better immersion. | **ON** | on / off |
| Show Compass HUD | Adds a compass heading to the player HUD. | **ON** | on / off |
| Teardrop Kiosk Flags | Bright teardrop banners with a symbol and a word at every NPC kiosk. Off: the classic hanging flags. Applies to flags placed after the change (a restart refreshes all). | **ON** | on / off |
| Chat Text Scale | Adjusts the size of the multiplayer chat box. | **ON** (1.3) | Vanilla (100%) / Large (130%) / Huge (175%) / Max (200%) |
| Chat Fade Delay | Controls how long messages stay visible before fading out. | **ON** (25) | Vanilla (10s) / Extended (25s) / Long (45s) / Persistent (90s) |
| Auto-Skip Guided Tour | Skips the singleplayer tutorial prompts when the map loads. | **ON** | on / off |
| Active FSCore theme (Default, Warm Amber, Light) | Selects which colour palette and font kit the FSCore HUD, phone, and overlays use. Each theme is a coherent visual identity - swap on the fly without restarting. | **ON** ("fscore_default") | on / off |

## VEHICLE

| Rule | What it does | Default | Choices |
|---|---|---|---|
| Require Manual Implement Attach | Players must stand on foot near the hitch to connect equipment. | OFF | on / off |
| Disable AI Workers | Globally blocks the 'Hire Worker' action. | OFF | on / off |
| Block Ignition on Written-Off Vehicles | Engines will not start once damage reaches 100%. | **ON** | on / off |
| Fatigue Affects Vehicle Power | Dynamically reduces engine torque when the driver's fatigue is high. | OFF | on / off |
| Realistic Refuelling (Hand Nozzle) | Disables in-vehicle refuelling at fuel triggers. Get out, press R at a pump or fuel tank to take the nozzle, and aim it at the vehicle to fuel. | OFF | on / off |
| Split Fuel Billing | Fuel for farm machinery is charged to the vehicle's farm account. Personal road vehicles pay from the driver's cash, and farm-fuel locations refuse them (dyed diesel). | OFF | on / off |
| Market-Based Fuel Pricing | Public station prices track the game's live diesel price times the selected retail markup, moving with difficulty and market swings. Stations with an admin-set price keep it. | **ON** (0.7) | Discount (0.7x) / Reduced (0.85x) / At Cost (1.0x) / Low Markup (1.1x) / Retail (1.2x) / Premium (1.35x) / Peak Markup (1.5x) |

## WORLD

| Rule | What it does | Default | Choices |
|---|---|---|---|
| Lock Time Scale | Forces a constant server time speed, overriding manual changes. | **ON** (0) | Off (players choose) / 1x (real-time) / 5x / 30x / 60x / 120x / 1000x |
| Auto-Skip Night-time | Speeds up time during the configured night hours. | **ON** ("aggressive") | Off / Mild (18:00->06:00 @ 30x) / Standard (18:00->06:00 @ 60x) / Fast (18:00->06:00 @ 120x) / Aggressive (18:00->06:00 @ 1000x) |
| Disable Sleep Triggers | Blocks players from using farmhouse beds to skip time. | **ON** | on / off |
| Require Fishing Licence | Players must hold a Fishing licence (sold at the bait shop, or granted in Settings) before they can cast. | **ON** | on / off |
| Disable Rain Harvest Penalty | Removes the vanilla yield reduction when harvesting in storms. | **ON** | on / off |
| Remove Map NPCs | Removes the decorative pedestrians walking around the map. | OFF | on / off |
| Enable Survival Needs System | Activates the core hunger, thirst, and fatigue loop. | **ON** | on / off |
| Eat / Drink Time | How long the hold-to-consume meter takes when eating food or drinking (seconds). Applies to all players. | **ON** (10) | Fast (3s) / Quick (5s) / Default (10s) / Standard (15s) / Slow (25s) / Realistic (45s) |
| Trim Overfilled Troughs | Troughs holding more of a food than its share are cut back to the share when the savegame loads and when this is switched on. The extra food is removed and not refunded. | OFF | on / off |
| Farm Fridge Size | Slots in each farm's shared fridge. Every member can stock it and take from it; only food, drink and dog food fit, and food in it goes stale at half speed. | **ON** (12) | Small (8 slots) / Standard (12 slots) / Large (16 slots) / Extra Large (20 slots) / Walk-in (24 slots) |
| Dog Patrol Animal Bonus (%) | Extra animal output (milk/eggs/wool/etc.) for a farm whose dog is on Farm Duty, cared for (all needs above 25%), and has a placed dog bed. Applies to every owned pen. | **ON** (10) | Off (0%) / 5% / 10% / 15% / 20% / 25% |
