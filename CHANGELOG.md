# TokenPanda 1.4.0 Beta

## Release status

TokenPanda 1.4.0 Beta promotes the fully validated 1.4.0 Alpha line, including the
Purchase History, realm-aware purchase records, RealmData integration, and the final
runtime localization refinements validated before release.

## Purchase History

- Added a complete account-wide WoW Token Purchase History.
- Successful WoW Token purchases can be captured automatically from the Blizzard purchase event.
- Purchases can also be added manually.
- Existing records can be edited by selecting a row.
- Records can be deleted with confirmation.
- Journalator WoW Token history can be imported from CSV.
- Built-in Import Help documents the current Journalator export workflow.
- Purchase records retain exact timestamp, price, character, realm, flavor, region, and origin metadata.
- Leaving Price blank in Add/Edit resolves the most recent historical price at or before the purchase timestamp when available.
- Purchase History can optionally display personal purchases on the historical chart.
- Purchase markers use the exact purchase timestamp and provide contextual hover information.
- Multiple purchases on the same calendar day are represented coherently in chart context.

## Realm-aware purchase records

- Purchase records now retain Realm information.
- Add/Edit provides Realm autocomplete while preserving free-text entry.
- Realm suggestions use TokenPandaTray RealmData when available, plus current/learned runtime sources.
- RealmData is maintained independently for Classic and Retail across US, EU, KR, and TW.
- Matchbox 2.0 continues to isolate Flavor + Region tuples and manual selection remains session-only.

## TokenPandaTray integration

Updating TokenPandaTray to 1.4.0 Beta is recommended for the complete realm-data experience.

Older Tray versions remain compatible with TokenPanda 1.4.0 through the existing legacy
fallback path, but realm-aware functionality can be limited when modern RealmData is not available.

**TokenPandaTray fallback support will be removed in the next TokenPanda version.**
Please update TokenPandaTray to the latest available version to keep full functionality.

## Historical data compatibility

- Modern historical data remains authoritative at:
  `Data/<Flavor>/<Region>/HistoricalData.lua`
- The 1.4.0 Beta addon package includes a neutral root `HistoricalData.lua` compatibility stub.
- The root file exists only so legacy TokenPandaTray output can still be loaded without a TOC warning.
- Retail and modern installations continue to use the Flavor + Region Data structure.
- Legacy fallback is scheduled for removal in TokenPanda 1.5.0.

## Localization and UI polish

- Visible Purchase History, Import, Add/Edit, Matchbox, Import Help, and update-notice text is localized across all 11 supported locales.
- Secondary windows now refresh correctly when the active TokenPanda Locale changes at runtime.
- Import helper/status text refreshes without overwriting active errors or completed import results.
- Add/Edit Price help refreshes without overwriting validation errors.
- Chart tooltips are temporarily suppressed while Import Help is open.
- Purchase History metadata tooltips are temporarily suppressed while Add/Edit is open.

Supported locales:
`enUS`, `deDE`, `esES`, `esMX`, `frFR`, `itIT`, `koKR`, `ptBR`, `ruRU`, `zhCN`, `zhTW`.

## Compatibility

- World of Warcraft Classic
- World of Warcraft Retail
- Regions: US, EU, KR, TW
- One addon package for both game flavors

## Packaging

Public addon package:

`TokenPanda-1.4.0-beta.zip`

The package contains one root folder, `TokenPanda/`, with `TokenPanda.toc` directly
inside it. Development backup files are excluded.
