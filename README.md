# TokenPanda

TokenPanda is an independent addon for **World of Warcraft Classic and Retail** that displays the current WoW Token price, recent price history, comparative data, approximate trend projections, alerts, and your own WoW Token Purchase History directly in game.

The project includes:

- **TokenPanda 1.5.0 Beta** — the in-game addon.
- **TokenPandaTray 1.5.0 Beta** — the portable Windows companion app used to synchronize and protect TokenPanda data.

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
- TokenPandaTray version awareness and update warning.
- Required-data validation for HistoricalData and RealmData.
- Improved critical-data recovery and protection.
- Cross-tuple historical viewing without artificial flat-line extension.
- Manual Refresh support for non-current tuples.
- Correct handling of WoW Token prices above 1,000,000 gold.
- Compact K formatting for very large graph-scale labels only.
- Regions: US, EU, KR, and TW.
- Eleven interface languages.

## Download TokenPanda 1.5.0 Beta

### 1. TokenPanda Addon

[![Download Addon](https://img.shields.io/badge/Download-TokenPanda_Addon-ffd700?style=for-the-badge&logo=github)](https://github.com/EZ-Mouse/TokenPanda/releases/download/v1.5.0-beta/TokenPanda-1.5.0-beta.zip)

Install the included `TokenPanda` folder in:

Classic:  
`World of Warcraft/_classic_/Interface/AddOns/`

Retail:  
`World of Warcraft/_retail_/Interface/AddOns/`

### 2. TokenPandaTray

[![Download Tray App](https://img.shields.io/badge/Download-TokenPandaTray-7aa2f7?style=for-the-badge&logo=windows)](https://github.com/EZ-Mouse/TokenPanda/releases/download/v1.5.0-beta/TokenPandaTray-1.5.0-beta.zip)

TokenPandaTray is the portable Windows companion app that synchronizes and protects the HistoricalData and RealmData used by TokenPanda.

**TokenPandaTray 1.5.0 or newer is required for the complete TokenPanda 1.5.0 data experience.**

TokenPanda 1.5.0 no longer uses the legacy root HistoricalData compatibility path. Modern Flavor + Region data is now required.

[View the full release and release notes](https://github.com/EZ-Mouse/TokenPanda/releases/tag/v1.5.0-beta)

## Current public Beta

`TokenPanda 1.5.0 Beta`  
`TokenPandaTray 1.5.0 Beta`

## Quick installation

1. Close World of Warcraft.
2. Extract `TokenPanda-1.5.0-beta.zip`.
3. Copy the `TokenPanda` folder into the appropriate AddOns directory.
4. Extract `TokenPandaTray-1.5.0-beta.zip`.
5. Run `TokenPandaTray.exe`.
6. Select your World of Warcraft folder.
7. Configure the Classic and Retail regions you want to synchronize.
8. Enable synchronization.
9. Start World of Warcraft and enter `/tokenpanda`.

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

TokenPanda can read the TokenPandaTray producer version from synchronized data and compare it with the minimum Tray version required by the addon.

If the detected Tray version is missing, legacy, or below the required version, TokenPanda can display a red **[!]** warning beside the active Flavor + Region selector.

Selecting the warning opens the TokenPandaTray Update Required notice.

## Required data

TokenPanda 1.5.0 validates the required data for the current Flavor + Region tuple.

Historical data:  
`Data/<Flavor>/<Region>/HistoricalData.lua`

Realm catalogs:  
`Data/<Flavor>/<Region>/RealmData.lua`

Both files are part of the modern TokenPanda data contract.

The previous root `HistoricalData.lua` compatibility path and addon legacy fallback logic have been removed.

## Data protection and recovery

TokenPandaTray protects the modern TokenPanda data structure and can recover missing, empty, invalid, or unusable required data.

Critical recovery remains available independently from the normal Smart mode synchronization pause.

Recovery can use valid local copies and configured backend sources while preserving the Flavor + Region data structure.

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

`TokenPanda-1.5.0-beta.zip`  
`TokenPandaTray-1.5.0-beta.zip`  
`SHA256SUMS.txt`

## Compatibility

- World of Warcraft Classic.
- World of Warcraft Retail.
- Windows 10 and Windows 11, 64-bit, for TokenPandaTray.
- Regions: US, EU, KR, and TW.
- Interface languages: enUS, deDE, esES, esMX, frFR, itIT, koKR, ptBR, ruRU, zhCN, zhTW.

## Privacy

TokenPandaTray does not require an account and does not request World of Warcraft or Battle.net credentials. It downloads public data and maintains TokenPanda local data files.

## Support and bug reports

Please use the repository's **GitHub Issues** section.

When reporting a synchronization problem, include:
- TokenPanda and TokenPandaTray versions;
- game flavor: Classic or Retail;
- selected region;
- whether World of Warcraft was running;
- the relevant TokenPandaTray log, when available.

## Independent project

TokenPanda is independent and unofficial. It is not affiliated with, sponsored by, authorized by, or endorsed by Blizzard Entertainment or by the operators of any public data service used by the project.

World of Warcraft, WoW, and Blizzard Entertainment are trademarks or registered trademarks of Blizzard Entertainment, Inc.

## Author

**EZ-Mouse Dev.**

> Obsessed with perfection.
