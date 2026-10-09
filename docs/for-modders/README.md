# FSCore - Notes for Mod Authors

FSCore is a single mod, but other mods can read from it and build on it through its public API. The [LICENSE](../../LICENSE) explicitly allows mods that interact with FSCore through that API.

## Where the API lives

Everything public is published on `g_currentMission.FSCore` once the map has loaded, one table per subsystem, for example:

- `g_currentMission.FSCore.Economy` (deposit, withdraw, balances for "cash", "personal" and "farm")
- `g_currentMission.FSCore.Identity` (profiles, names, licenses)
- `g_currentMission.FSCore.Inventory` (add and remove items, weight)
- `g_currentMission.FSCore.Reputation` (skills and levels)
- `g_currentMission.FSCore.Config` (`isRuleEnabled`, `getRuleValue`)

Events are published through `FSCore.subscribe(eventName, callback)`.

Detect FSCore at runtime and degrade gracefully when it is absent:

```lua
local core = g_currentMission ~= nil and g_currentMission.FSCore or nil
if core ~= nil and core.Economy ~= nil then
    core.Economy.deposit(userId, "personal", 250, "Delivery pay")
end
```

Do not declare FSCore as a hard `<dependency>` unless your mod cannot function without it.

## Rules of the road

- **Server-authoritative.** Anything that changes money, items or profiles must run on the server. Send an event from the client and validate on the server.
- **No protected calls.** FSCore APIs never raise Lua errors; failures come back as `nil`, `false` or an empty table. Check return values instead of wrapping calls in `pcall`, which the ModHub review also rejects.
- **Read-only payloads.** Treat event payload tables as read-only and never store references to tables FSCore hands you; copy what you need.
- **No copying.** Integrate through the API. Extracting or embedding FSCore code or assets is not permitted.

## Getting help

Use the [Integration Help template](https://github.com/RocklandUSA/FS25_FSCore/issues/new?template=integration_help.yml) with the Lua you tried, what you expected and what happened. More material is on [fscore.gg](https://fscore.gg/).
