# FSCore - Notes for Mod Authors

FSCore is a single mod, but other mods can read from it and build on it through its public API. The [LICENSE](../../LICENSE) explicitly allows mods that interact with FSCore through that API.

These notes match FSCore 1.0.0.0.

## Where the API lives

Everything public is published on `g_currentMission.FSCore` once the map has loaded, one table per subsystem, for example:

- `g_currentMission.FSCore.Economy`: `isReady()`, `deposit(userId, amount, account, reason)`, `withdraw(userId, amount, account, reason)`, `getBalance(userId, account)`. The account is `"cash"` (the pocket wallet), `"personal"` (the player's current account, the default) or `"farm"` (the game's own farm account). `INTEGRATION_VERSION` is `1`.
- `g_currentMission.FSCore.Identity`: profiles and names (`getProfile`, `getFullName`, `getSpecialization`), licences (`hasLicense`, `getLicenses`)
- `g_currentMission.FSCore.Inventory`: items (`registerItem`, `addItem`, `removeItem`, `hasItem`, `getItems`, `getWeight`)
- `g_currentMission.FSCore.Reputation`: skills and levels (`addXP`, `getXP`, `getLevel`, `getTitle`, `getLeaderboard`, `hasMinLevel`)
- `g_currentMission.FSCore.Config`: the server rules (`isRuleEnabled(ruleId)`, `getRuleValue(ruleId)`). The rule ids are listed in the [settings reference](../for-admins/SETTINGS.md); module switches are the `enable_*` ids

Events are published through `g_currentMission.FSCore.subscribe(eventName, callback)`, which returns an id for `unsubscribe(id)`.

Detect FSCore at runtime and degrade gracefully when it is absent:

```lua
local core = g_currentMission ~= nil and g_currentMission.FSCore or nil
if core ~= nil and core.Economy ~= nil and core.Economy.isReady() then
    core.Economy.deposit(userId, 250, "personal", "Delivery pay")
end
```

Do not declare FSCore as a hard `<dependency>` unless your mod cannot function without it. A module the server switched off may have no table at all, so check before you call.

## Rules of the road

- **Server-authoritative.** Anything that changes money, items or profiles must run on the server. Send an event from the client and validate on the server.
- **Real value only.** `deposit` is for genuine value exchange the way the base game adds money (a sale, a prize, a contract payout), not for creating money from nothing.
- **No protected calls.** FSCore APIs never raise Lua errors; failures come back as `nil`, `false` or an empty table. Check return values instead of wrapping calls in `pcall`, which the ModHub review also rejects.
- **Read-only payloads.** Treat event payload tables as read-only and never store references to tables FSCore hands you; copy what you need.
- **No copying.** Integrate through the API. Extracting or embedding FSCore code or assets is not permitted.

## Getting help

Use the [Integration Help template](https://github.com/RocklandUSA/FS25_FSCore/issues/new?template=integration_help.yml) with the Lua you tried, what you expected and what happened. More material is on [fscore.gg](https://fscore.gg/), or ask on the [Discord](https://discord.gg/xd9B6uSEjV).
