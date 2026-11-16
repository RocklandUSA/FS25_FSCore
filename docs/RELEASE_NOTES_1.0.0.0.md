# FSCore 1.0.0.0 - Release Notes

**Status:** prepared for the GIANTS ModHub submission in November 2026. Not yet approved or published. These notes become the release text once GIANTS publishes 1.0.0.0.

FSCore - Rural Life Simulation Framework turns a Farming Simulator 25 save into a living town. Your farm is only the beginning: you are a person in the town, with a phone, a wage, a home, a reputation and neighbours to build with.

- **Game:** Farming Simulator 25 on PC and Mac, latest game update (1.25.1 or newer)
- **Modes:** singleplayer, multiplayer, dedicated servers
- **Languages:** English, German, Polish, French
- **Size of the system:** 50 switchable modules, 44 phone apps, 93 live settings

## Highlights

### Your phone runs your life
Press `/` and a full smartphone slides up. Text friends and farms, post to FarmSnap, follow Village Chat, check the weather and calendar, handle your money in Finances (every loan with its details) and follow turn-by-turn Navigation. Your ID, licences, keys, homes, garage, backpack, recipes, dog, jobs, reputation and the town's news are a tap away. For the farm: PlotView reads every field, HerdSync checks every barn, SimpliBarn puts cameras in the barns, and SiloView, Productions and Farm Stats show everything you own and produce.

### A home of your own
Lizard Realty lists the map's houses, to buy outright or with a mortgage. Furnish every room from almost 300 pieces of furniture, landscape the garden with nearly 90 plants and garden pieces, sit in your own chairs and recliners, hang flower boxes under the windows, and give spare keys to the people you trust.

### Build it yourself
Buy a building lot and the plans, set the site out, bring the pallets (the house kits come with a loaner forklift) and build stage by stage with hammer, cordless drill, trowel and paint roller: the Ranch House and the Harvest House with a colour scheme you choose at the end, garden sheds, greenhouses, pergolas, chicken coops, wood stores, compost bins and raised beds.

### A town that grows - together
- **AutoPlot** turns a Town Hall field into a planned neighbourhood with asphalt streets, street lights, picket fences, lawns and a FOR SALE sign on every lot. Every road gets a street name and every home an address.
- **Community projects that unlock features.** The whole server builds the town's big buildings, and each one opens something for everyone when it is finished:
  - **Car Dealership:** FSCore's dealership for player-owned vehicles (buying, test drives, customising and repairs at the mechanic) and the Shiftit towing calls
  - **Post Office & Parcel Depot:** the Shiftit mail and parcel rounds
  - **Self-Storage Yard:** big storage units to rent
  - **Co-op Grain Elevator:** the **Farmers Co-op**, paying 10 % more than the best price on the map for grain, with massive storage and a working truck scale. The largest build, with tower-crane lifts, a man basket and slip-form concrete pours

  Town Hall pays for the materials and the shifts, every pallet is tracked to its site, and the top builders earn Golden, Silver and Bronze Hammer trophies. Administrators set the projects out in the Admin Hub, see them in Map Audit and can override any unlock with `fscUnlock`.

### Work and wages
- **Shiftit company jobs:** mail rounds served from the driver's seat, parcel rounds, propane deliveries with the hose reel, towing calls with the rollback, kerbside refuse collection, warehouse forklift shifts with a customer pick-up board, and Lizard Lawncare mowing contracts. Company work clothes, and ranks that pay up to 35 % more.
- **Giggit** gigs (deliveries, pallet freight, towing, junk cleanup, power washing) and **Farm Eats** bakery and pizza deliveries.
- **Time clocks** with hourly pay, payroll, roles and permissions, and hiring players onto your farm.

### Become somebody
Nine skill trees (Agronomy, Husbandry, Forestry, Logistics, Mechanical, Business, Community, Angling, Mining), ten levels each with titles to earn. Leaderboards, Competitions with an overall standing, a colour-coded overall level on name tags and the My ID card, and for the farm work itself: Farm Points, 15 farming ranks, medals and a Farmer of the Week.

### Into the mine
Ride the lift down and dig the mine out a section at a time. Follow the ore veins with pickaxe and rock drill by the light of your headlamp and the lanterns, lay track for the ore carts, find fossils, geodes and diamonds, smelt ingots at the mine forge and craft rings, pendants and building materials. The Mine app shows the shaft map, the crew at the face, the compressor's fuel and your collection.

### Money that matters
Cash in your pocket, current, savings and business accounts, ATMs, invoices between players and farms, income tax, VAT and property tax, a credit rating, mortgages and dealership finance.

### Survive and thrive
Hunger, thirst and fatigue. Food that goes stale and spoils. Farm fridges, storage lockers and crates to carry or fork-lift. A backpack (`F10` or `Alt` + `I`), crafting at workbenches, shops and fuel stations with hand-nozzle refuelling, and a radial menu (`F9`) for emotes, quick actions and dog commands.

### Your own wheels
Dealership with finance, vehicle keys and locks for personal and farm vehicles, a personal garage, farm garages that park and bring out your machines, vehicle rentals, a mechanic, and equipment licences (Ag Operator, Truck, Forestry) for servers that want them.

### The great outdoors
Fishing with bait that reacts to weather and water, nine species, fish buyers, marina boards and tournaments; boats and fishing rafts to rent; farm dogs adopted from the Pet Shelter that follow, patrol and boost your animal pens on farm duty; scavenging and salvaging; and the EGG RUN arcade cabinet, played on the cabinet's own screen.

### A town that changes with the seasons
Seasonal Street Lights for Christmas, New Year, Lunar New Year, Carnival, Halloween, the harvest and more, by the real or the in-game calendar, north or south of the equator. Map Essentials adds vending machines, bins and decorations to any map.

### Ready on every base-game map
Riverbend Springs, Zielonka, Hutan Pantai, Kinlaig and Catuaí come set up on the first load of a new save.

### Built for server owners
The Admin Hub (`F6`) opens every admin tool, from Map Audit and Community Projects to moderation and the placement editors. The FSCore Settings page has 93 live settings, among them a switch for every module. FSCore does not monitor or track anyone.

## Notes for server owners

- On a server with the Construction module on, the features above that belong to a community project stay locked until the community has built it. Set the projects out, or open a feature by hand with `fscUnlock <dealership|postal|storage|coop> on`. With Construction off nothing is locked. See [Community projects and map setup](for-admins/COMMUNITY_PROJECTS.md).
- Server and clients must run the same version. Restart the server after updating, and let it finish loading before players join.
- References: [settings](for-admins/SETTINGS.md), [console commands](for-admins/CONSOLE_COMMANDS.md), [installation](for-admins/INSTALL.md).

## Not in 1.0.0.0

The Fire Station and Public Works community projects, and the other ideas on the 1.1 list in the [README](../README.md#planned-for-11-not-in-1000), are planned for a later update and are not part of this release.
