# TokenPanda

TokenPanda is an independent addon for **World of Warcraft Classic and Retail** that displays the current WoW Token price, recent price history, comparative data, approximate trend projections, alerts, and your own WoW Token Purchase History directly in game.

The project includes:

- **TokenPanda 1.5.1 Beta** — the in-game addon.
- **TokenPandaTray 1.5.1 Beta** — the portable Windows companion app used to synchronize and protect TokenPanda data.

## What's new in 1.5.1 Beta?

### TokenPanda Addon

- Added recommended and required TokenPandaTray update indicators.
- Improved version comparison for Alpha, Beta, and final releases.
- Improved update notification presentation.
- Updated changelog and download information.
- Updated in-game download links to always point to the latest official release.
- Updated translations across all eleven supported languages.

### TokenPandaTray

- Fixed historical data synchronization issues.
- Improved historical data recovery.
- Improved data consistency and integrity.
- Optimized background operations and resource usage.
- Improved synchronization scheduling and retry handling.
- General performance and stability improvements.

## Main features

- Support for World of Warcraft Classic and Retail.
- Current WoW Token price.
- Historical periods: 3D, 7D, 14D, 1M, 3M, 6M, and ALL.
- Comparison with the previous equivalent period.
- Approximate 6-hour and 12-hour trend projections in the 3D view.
- Possible rebound and trend-change notifications.
- Independent upper and lower notification areas.
- Minimized, normal, analysis, and integrated views.
- Independent saved position for each view.
- Visual alerts for trends, proximity to lows, and new lows.
- Matchbox 2.0 data-source selection.
- Account-wide WoW Token Purchase History.
- Automatic capture of successful WoW Token purchases.
- Manual Add, Edit, and Delete purchase management.
- Journalator CSV import with built-in Import Help.
- Optional purchase markers on the historical chart.
- Character, Realm, Flavor, Region, timestamp, price, and origin metadata.
- Realm-aware purchase records and Realm autocomplete.
- TokenPandaTray RealmData synchronization.
- TokenPandaTray version awareness.
- Recommended and required TokenPandaTray update notifications.
- Color-coded contextual `[!]` update indicators.
- Alpha, Beta, and final version comparison.
- Required-data validation for HistoricalData and RealmData.
- Improved critical-data recovery and protection.
- Improved historical data synchronization.
- Independent synchronization of Classic and Retail regions.
- Optimized background operations and resource usage.
- Improved synchronization scheduling and retry handling.
- Cross-tuple historical viewing without artificial flat-line extension.
- Manual Refresh support for non-current tuples.
- Correct handling of WoW Token prices above 1,000,000 gold.
- Compact K formatting for very large graph-scale labels only.
- Regions: US, EU, KR, and TW.
- Eleven interface languages.

## Download TokenPanda 1.5.1 Beta

### 1. TokenPanda Addon

[![Download Addon](https://img.shields.io/badge/Download-TokenPanda_Addon-ffd700?style=for-the-badge&logo=github)](https://github.com/EZ-Mouse/TokenPanda/releases/download/v1.5.1-beta/TokenPanda-1.5.1-beta.zip)

Install the included `TokenPanda` folder in:

Classic:  
`World of Warcraft/_classic_/Interface/AddOns/`

Retail:  
`World of Warcraft/_retail_/Interface/AddOns/`

The addon is also available on [CurseForge](https://www.curseforge.com/wow/addons/tokenpanda).

### 2. TokenPandaTray

[![Download Tray App](https://img.shields.io/badge/Download-TokenPandaTray-7aa2f7?style=for-the-badge&logo=windows)](https://github.com/EZ-Mouse/TokenPanda/releases/download/v1.5.1-beta/TokenPandaTray-1.5.1-beta.zip)

TokenPandaTray is the portable Windows companion app that synchronizes and protects the HistoricalData and RealmData used by TokenPanda.

**TokenPandaTray 1.5.1 Beta or newer is required for TokenPanda 1.5.1 Beta.**

Starting with TokenPanda 1.5.0, the legacy root HistoricalData compatibility path is no longer supported. Modern Flavor + Region data is required.

TokenPandaTray 1.5.1 introduces significant improvements to synchronization reliability, historical data recovery, performance, and overall stability.

[View the latest official release and release notes](https://github.com/EZ-Mouse/TokenPanda/releases/latest)

## Current public Beta

`TokenPanda 1.5.1 Beta`  
`TokenPandaTray 1.5.1 Beta`

## Quick installation

1. Close World of Warcraft.
2. Extract `TokenPanda-1.5.1-beta.zip`.
3. Copy the `TokenPanda` folder into the appropriate AddOns directory.
4. Extract `TokenPandaTray-1.5.1-beta.zip`.
5. Run `TokenPandaTray.exe`.
6. Select your World of Warcraft folder.
7. Configure the Classic and Retail regions you want to synchronize.
8. Enable synchronization.
9. Start World of Warcraft and enter `/tokenpanda`.

TokenPandaTray is portable and requires no traditional installation.

## Updating an existing installation

1. Fully close World of Warcraft and TokenPandaTray.
2. Back up your existing TokenPanda historical data.
3. Update the TokenPanda addon without overwriting valid synchronized historical data with empty bundled files.
4. Replace the previous TokenPandaTray executable with the latest version.
5. Start TokenPandaTray.
6. Review your configured Classic and Retail regions.
7. Synchronize the enabled data sources.
8. Start World of Warcraft.

Do not mix addon code files from different versions.

Always obtain the latest TokenPandaTray version from the [official GitHub release](https://github.com/EZ-Mouse/TokenPanda/releases/latest).

## Purchase History

Press **[H]** to open Purchase History.

TokenPanda can:

- automatically record successful WoW Token purchases;
- add purchases manually;
- edit a record by selecting its row;
- delete records with confirmation;
- import Journalator WoW Token CSV exports;
- show purchase markers on the chart;
- retain Character and Realm metadata.

## Matchbox 2.0

Press the Flavor + Region selector, such as **[C · US]**, to inspect available data sources for Classic/Retail and US/EU/KR/TW.

Manual selections apply only to the current session. After `/reload` or a complete restart, TokenPanda returns to the data source matching the current WoW client.

When inspecting a tuple different from the currently running WoW client, TokenPanda stops the graph at the timestamp of the last available sample instead of extending stale data as an artificial flat line.

A **[ Refresh ]** action is available for non-current tuples. Refreshing the addon only reloads data already written by TokenPandaTray, so force a data update in TokenPandaTray first when fresh external-tuple data is required.

## TokenPandaTray version awareness

TokenPanda can read the TokenPandaTray producer version from synchronized data and compare it with the minimum required and recommended Tray versions.

Starting with TokenPanda 1.5.1, update notifications distinguish between recommended and required updates.

| Indicator | Status | Description |
| --- | --- | --- |
| No update indicator | Up to date | The detected producer version satisfies the current update requirements. |
| 🟠 **[!]** | Update recommended | A newer TokenPandaTray version is recommended. |
| 🔴 **[!]** | Update required | The detected producer version does not satisfy the minimum version requirement. |

### Recommended update

The orange indicator remains static and provides information about the recommended TokenPandaTray version when selected.

### Required update

The red indicator pulses to highlight that an update is required and may display an automatic update notification.

Selecting the indicator opens a detailed notice containing:

- detected TokenPandaTray producer version;
- required or recommended version;
- HistoricalData availability;
- RealmData availability;
- official download link.

Data availability and integrity warnings remain available independently of update notifications.

Existing valid historical data remains accessible while an update notification is active.

After updating TokenPandaTray, synchronize your configured data sources and reload the World of Warcraft interface using `/reload`.

## Required data

TokenPanda validates the required data for the current Flavor + Region tuple.

Historical data:  
`Data/<Flavor>/<Region>/HistoricalData.lua`

Realm catalogs:  
`Data/<Flavor>/<Region>/RealmData.lua`

Both files are part of the modern TokenPanda data contract.

The previous root `HistoricalData.lua` compatibility path and addon legacy fallback logic were removed in TokenPanda 1.5.0.

The modern data structure remains unchanged in TokenPanda 1.5.1.

## Data protection and recovery

TokenPandaTray protects the modern TokenPanda data structure and can recover missing, empty, invalid, or unusable required data.

Version 1.5.1 improves:

- historical data synchronization;
- recovery of available historical samples;
- preservation of existing valid records;
- independent synchronization of Flavor + Region data sources;
- synchronization scheduling and retry handling;
- background operations and resource usage.

Recovery can use valid local copies and configured backend sources while preserving the Flavor + Region data structure.

Historical recovery depends on the valid local data and historical information available from the data provider.

## Smart mode

Smart mode detects whether World of Warcraft is running.

Normal periodic synchronization can pause while WoW is running and resume when WoW is not running.

Critical data protection remains available independently of the normal synchronization pause.

## Chart reference

- **Yellow line:** current-period price history.
- **Red line:** previous equivalent period.
- **Gray line:** approximate projected trend.
- **Purchase marker:** optional personal WoW Token purchase indicator.

TokenPanda displays the real WoW Token price as a complete gold value and does not abbreviate or reinterpret it.

For very large values, only the graph's Y-axis scale may use compact `K` labels to preserve readability. The actual price, historical values, hover tooltips, Purchase History, and variation remain complete and precise.

## Projection notice

Projected values represent only a possible trend. They are not guaranteed future prices and should not be used as the sole basis for a decision.

## Downloads

Public release assets:

| File | Description |
| --- | --- |
| [TokenPanda-1.5.1-beta.zip](https://github.com/EZ-Mouse/TokenPanda/releases/download/v1.5.1-beta/TokenPanda-1.5.1-beta.zip) | World of Warcraft addon |
| [TokenPandaTray-1.5.1-beta.zip](https://github.com/EZ-Mouse/TokenPanda/releases/download/v1.5.1-beta/TokenPandaTray-1.5.1-beta.zip) | Portable Windows companion application |
| [TokenPanda-SHA256SUMS.txt](https://github.com/EZ-Mouse/TokenPanda/releases/download/v1.5.1-beta/TokenPanda-SHA256SUMS.txt) | Addon integrity verification |
| [TokenPandaTray-SHA256SUMS.txt](https://github.com/EZ-Mouse/TokenPanda/releases/download/v1.5.1-beta/TokenPandaTray-SHA256SUMS.txt) | Tray integrity verification |

SHA-256 checksums are provided to verify the integrity of the downloaded packages.

[View the latest official release](https://github.com/EZ-Mouse/TokenPanda/releases/latest)

## Compatibility

- World of Warcraft Classic.
- World of Warcraft Retail.
- Windows 10 and Windows 11, 64-bit, for TokenPandaTray.
- TokenPandaTray 1.5.1 Beta or newer.
- Regions: US, EU, KR, and TW.
- Interface languages: enUS, deDE, esES, esMX, frFR, itIT, koKR, ptBR, ruRU, zhCN, zhTW.

## Privacy

TokenPandaTray:

- does not require an account;
- does not request World of Warcraft or Battle.net credentials;
- does not sign in to Battle.net;
- does not modify the World of Warcraft executable;
- downloads public data and maintains TokenPanda local data files.

Always download TokenPanda and TokenPandaTray from their official distribution channels.

## Support and bug reports

Please use the repository's [GitHub Issues](https://github.com/EZ-Mouse/TokenPanda/issues) section.

When reporting a synchronization problem, include:

- TokenPanda and TokenPandaTray versions;
- game flavor: Classic or Retail;
- selected region;
- whether World of Warcraft was running;
- the relevant TokenPandaTray log, when available.

## Official distribution channels

- [GitHub — Latest Release](https://github.com/EZ-Mouse/TokenPanda/releases/latest)
- [CurseForge — TokenPanda](https://www.curseforge.com/wow/addons/tokenpanda)

## Independent project

TokenPanda is independent and unofficial. It is not affiliated with, sponsored by, authorized by, or endorsed by Blizzard Entertainment or by the operators of any public data service used by the project.

World of Warcraft, WoW, and Blizzard Entertainment are trademarks or registered trademarks of Blizzard Entertainment, Inc.

## Author

**EZ-Mouse Dev.**

> Obsessed with perfection.
