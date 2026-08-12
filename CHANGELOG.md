# TokenPandaTray 1.4.0 Beta

## Release status

This Beta promotes the validated `1.4.0-alpha-40` TokenPandaTray implementation to the
shared TokenPanda 1.4.0 release line without changing its synchronization, recovery,
RealmData provider, or watchdog behavior.

## HistoricalData synchronization and recovery

For every enabled Flavor + Region tuple, TokenPandaTray maintains:

`TokenPanda\Data\<Flavor>\<Region>\HistoricalData.lua`

The HistoricalData watchdog detects missing, unreadable, empty, invalid, or degraded
primary data and can recover from the best valid local catalog before requiring HTTP.

Recovery candidates include:
1. a valid copy of the same tuple from another WoW installation;
2. valid `.bak` data;
3. the backend when no usable local catalog exists.

Writers avoid replacing a good backup with invalid or empty seed data.

## RealmData synchronization

TokenPandaTray maintains:

`TokenPanda\Data\<Flavor>\<Region>\RealmData.lua`

for enabled Classic/Retail + US/EU/KR/TW tuples.

The validated provider pipeline includes:
1. WoWAnalyzer GitHub-backed realm catalogs;
2. WoWAudit GitHub-backed realm catalogs;
3. the legacy wow-realm-status GraphQL provider;
4. the legacy Blizzard Realm Status HTML provider.

Successful catalogs are merged and deduplicated. If all providers fail, the last valid
RealmData is preserved and the tuple remains retryable.

Missing, empty, or invalid RealmData can trigger startup recovery independently per tuple.

## Smart mode

Smart mode detects whether World of Warcraft is running. Normal periodic synchronization
can pause while WoW is active and resume when WoW is not running. Critical data protection
continues to operate independently of the normal synchronization pause.

## Legacy compatibility

TokenPanda 1.4.0 is the final TokenPanda release line that retains legacy fallback compatibility.

The root:

`TokenPanda\HistoricalData.lua`

is maintained only for that compatibility path. Modern TokenPanda data remains under
`Data/<Flavor>/<Region>/`.

Fallback support is planned for removal in TokenPanda 1.5.0.

## Packaging

Public package contains exactly:
- `TokenPandaTray.exe`
- `SHA256.txt`
