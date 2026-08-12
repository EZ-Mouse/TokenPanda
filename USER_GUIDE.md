# TokenPanda User Guide

## What is TokenPanda?

TokenPanda is an independent addon for **World of Warcraft Classic and Retail** that displays the current WoW Token price, recent price history, comparisons, approximate trend projections, alerts, and your own WoW Token Purchase History directly inside the game.

**TokenPandaTray** is the portable Windows companion application used to download, synchronize, protect, and maintain the historical and realm data used by TokenPanda.

This guide applies to:

```text
TokenPanda 1.4.0 Beta
TokenPandaTray 1.4.0 Beta
```

> Updating TokenPandaTray to 1.4.0 Beta is strongly recommended for the complete realm-aware experience. Older Tray versions remain compatible with TokenPanda 1.4.0 through the legacy fallback path, but some realm-aware features may be limited.
>
> Legacy TokenPandaTray fallback support will be removed in the next TokenPanda version.

---

## Compatibility

### Supported game versions

- World of Warcraft Classic
- World of Warcraft Retail

### Supported regions

- US
- EU
- KR
- TW

### Supported interface languages

- enUS
- deDE
- esES
- esMX
- frFR
- itIT
- koKR
- ptBR
- ruRU
- zhCN
- zhTW

### TokenPandaTray requirements

- Windows 10 or Windows 11
- 64-bit
- No traditional installation required

---

## Installation

### 1. Install the addon

1. Close World of Warcraft.
2. Extract:

```text
TokenPanda-1.4.0-beta.zip
```

3. Copy the included `TokenPanda` folder into the appropriate AddOns directory.

Classic:

```text
World of Warcraft/_classic_/Interface/AddOns/
```

Retail:

```text
World of Warcraft/_retail_/Interface/AddOns/
```

The final path must be:

```text
Interface/AddOns/TokenPanda/TokenPanda.toc
```

Avoid creating a duplicated folder such as:

```text
AddOns/TokenPanda/TokenPanda/TokenPanda.toc
```

---

### 2. Start TokenPandaTray

1. Extract:

```text
TokenPandaTray-1.4.0-beta.zip
```

2. Run:

```text
TokenPandaTray.exe
```

3. Select your World of Warcraft folder.
4. Configure the Classic and Retail regions you want to synchronize.
5. Enable synchronization.

TokenPandaTray is portable and requires no traditional installation.

For the complete TokenPanda 1.4.0 experience, use the matching 1.4.0 Beta Tray.

---

## Open TokenPanda

Enter:

```text
/tokenpanda
```

or use the minimap icon.

---

## Main controls

- **Minimap left-click:** show or hide TokenPanda.
- **Minimap right-click:** show or hide the minimap menu.
- **Drag minimap icon:** move it.
- **Minimize button:** switch to the compact view.
- **Right-click minimize button:** switch between normal and analysis views.
- Each view keeps its own saved position.
- **[H]:** open Purchase History.
- **Flavor / Region selector**, such as **[C · US]:** open Matchbox 2.0.
- **Period selector:** choose the historical time range shown on the graph.

---

## Main window

The main TokenPanda window shows:

- current WoW Token price;
- recent price variation;
- selected Classic/Retail + region data source;
- approximate age of the current data;
- historical price graph;
- previous-period comparison;
- approximate projected trend when available;
- upper price-behavior notifications;
- lower chart/rebound notifications;
- personal purchase markers when enabled.

---

## Chart

Available periods:

```text
3D · 7D · 14D · 1M · 3M · 6M · ALL
```

### Chart lines

- **Yellow line:** current period.
- **Red line:** previous equivalent period when comparison is enabled.
- **Gray line:** approximate projected trend when projection is available.

### Previous-period comparison

Use the comparison checkbox to show or hide the previous equivalent period.

When enabled, TokenPanda can compare the current point with the previous-period point and show:

- current-period price;
- previous-period price;
- absolute difference;
- percentage difference.

### Hover information

Move the mouse over the graph to inspect contextual information such as:

- date;
- time;
- current-period price;
- previous-period price;
- difference;
- purchase information when a personal Token purchase is relevant to that point.

### Projection

Approximate projection is available in the 3D chart.

It can represent:

- 6-hour projection;
- 12-hour projection.

Projected values are analytical estimates only. They are not guaranteed future prices.

---

## Price and trend notifications

TokenPanda uses two independent notification areas.

### North Notification

The upper notification describes **price behavior**.

Examples include:

- proximity to a minimum;
- reaching a minimum;
- new minimum;
- other price-related attention states.

Example:

```text
Near the minimum!
```

### South Notification

The lower notification describes **chart behavior and rebound/trend signals**.

Examples include:

- possible upward rebound;
- possible downward rebound;
- confirmed upward rebound;
- confirmed downward trend change.

These signals are based on recent historical data and can change as new data arrives.

---

## Matchbox 2.0

Press the Flavor + Region selector, for example:

```text
[C · US]
```

to open Matchbox 2.0.

Matchbox 2.0 displays available data sources for:

### Classic

- US
- EU
- KR
- TW

### Retail

- US
- EU
- KR
- TW

It shows:

- available and unavailable tuples;
- current WoW client Flavor and Region;
- currently displayed data source;
- manual selection state.

Manual selections are **session-only**.

After:

```text
/reload
```

or a complete WoW restart, TokenPanda returns to the data source that matches the current WoW client.

---

## Purchase History

Press:

```text
[H]
```

to open Purchase History.

Purchase History is account-wide and realm-aware.

The list displays:

- Date
- Price

Each purchase can also retain metadata such as:

- Character
- Realm
- Flavor
- Region
- Origin
- Exact timestamp

---

## Automatic WoW Token purchase capture

TokenPanda can automatically record successful WoW Token purchases.

When Blizzard confirms a successful purchase, TokenPanda can store:

- exact purchase time;
- price;
- character;
- realm;
- game Flavor;
- region;
- purchase origin.

Each successful purchase is stored as an individual record.

---

## Add a purchase manually

In Purchase History, press:

```text
[ Add ]
```

Available fields include:

- Date
- Time
- Price
- Character
- Realm

### Leaving Price blank

Price can be left blank.

When possible, TokenPanda resolves the most recent historical WoW Token price at or before the specified purchase timestamp.

TokenPanda never uses a future historical sample for this lookup.

If no suitable previous historical sample exists, enter the price manually.

---

## Edit a purchase

To edit an existing purchase:

1. Open Purchase History.
2. Click the purchase row.
3. Edit the required fields.
4. Save the changes.

The same Price behavior used by Add also applies to Edit.

---

## Delete a purchase

Use the red:

```text
[x]
```

control beside a purchase.

TokenPanda asks for confirmation before removing the record.

---

## Realm autocomplete

The Realm field in Add/Edit supports autocomplete.

Suggestions can come from:

- RealmData synchronized by TokenPandaTray;
- the current realm;
- realms already learned from Purchase History;
- limited runtime Blizzard realm information.

The Realm field always accepts free text.

Autocomplete supports normal mouse and keyboard interaction, including:

- mouse hover;
- click;
- mouse wheel;
- arrow keys;
- Tab;
- Enter.

---

## Purchase metadata

Hovering Purchase History entries can show additional purchase metadata such as:

```text
WoW Token purchase
Character     Bankdir
Realm         Pagle
Source        TokenPanda
```

While Add/Edit is open, Purchase History metadata tooltips are temporarily disabled so they do not overlap the editor.

---

## Show purchases on the chart

Purchase History includes:

```text
[ Show on chart ]
```

When enabled, TokenPanda can display personal WoW Token purchases on the historical graph.

A purchase is represented by a small purchase marker at the purchase timestamp.

Hovering relevant chart positions can show information such as:

- purchase price;
- purchase date;
- purchase time;
- contextual current-period information.

If several purchases occurred on the same calendar day, TokenPanda can represent them together contextually.

---

## Import purchases from Journalator

Purchase History includes:

```text
[ Import ]
```

This allows WoW Token history to be imported from a Journalator CSV export.

### Journalator workflow

1. Open Journalator.
2. Select **WoW Tokens**.
3. Choose the period you want to export:
   - All Time
   - Last Year
   - Last 6 Months
   - Last 3 Months
   - Last Week
   - Last Day
   - Last Hour
4. Wait until Journalator finishes loading the requested data.
5. Click:

```text
[ Export Results ]
```

6. In the export window, press `Ctrl+A` if necessary.
7. Press `Ctrl+C` to copy the CSV.
8. Return to TokenPanda.
9. Open Purchase History.
10. Click:

```text
[ Import ]
```

11. Paste the CSV.
12. Import the records.

Journalator may change its interface or export workflow in future versions. If the current Journalator interface no longer matches these steps, refer to the current Journalator documentation.

---

## Import Help

Beside Import, TokenPanda includes:

```text
[ ? ]
```

This opens the built-in Import Help window with the current Journalator export procedure.

While Import Help is open, graph tooltips are temporarily disabled so they do not overlap the help window.

---

## HistoricalData

Modern TokenPanda historical data is stored independently by game Flavor and region:

```text
Data/<Flavor>/<Region>/HistoricalData.lua
```

Examples:

```text
Data/Classic/US/HistoricalData.lua
Data/Retail/EU/HistoricalData.lua
```

This keeps Classic and Retail history separated and prevents cross-flavor or cross-region contamination.

TokenPanda 1.4.0 also includes a neutral root:

```text
HistoricalData.lua
```

only for legacy TokenPandaTray fallback compatibility.

This legacy fallback path will be removed in the next TokenPanda version.

---

## RealmData

TokenPandaTray 1.4.0 can maintain Realm catalogs using:

```text
Data/<Flavor>/<Region>/RealmData.lua
```

RealmData is used by realm-aware Purchase History features such as Realm autocomplete.

RealmData is maintained separately for supported:

- Classic versions;
- Retail versions;
- US;
- EU;
- KR;
- TW.

Updating TokenPandaTray to 1.4.0 Beta is recommended to ensure these RealmData files are available.

---

## TokenPandaTray synchronization

TokenPandaTray maintains TokenPanda data for the Classic/Retail + Region combinations you enable.

It can synchronize:

- HistoricalData;
- RealmData.

It also includes protection for missing, invalid, empty, or degraded historical files and can recover usable local data when possible before requesting a fresh copy.

### Smart mode

Smart mode detects whether World of Warcraft is running.

Normal periodic synchronization can pause while WoW is running and resume when WoW is not running.

Critical data protection remains independent from the normal synchronization pause.

---

## “No history”

If TokenPanda shows no historical data:

1. Check that TokenPandaTray is running.
2. Confirm synchronization is enabled.
3. Verify the selected World of Warcraft folder.
4. Verify the correct Classic/Retail Flavor and region.
5. Wait for the first synchronization.
6. Check the active data source in Matchbox 2.0.
7. Use:

```text
/reload
```

if WoW was already open when the historical file was updated.

---

## Realm autocomplete is missing or incomplete

1. Update TokenPandaTray to 1.4.0 Beta.
2. Confirm the corresponding Classic/Retail + Region tuple is enabled.
3. Allow TokenPandaTray to synchronize RealmData.
4. Restart or `/reload` WoW if needed.
5. Remember that the Realm field still accepts free text even without RealmData.

---

## Updating

1. Fully close World of Warcraft.
2. Close TokenPandaTray.
3. Replace the old TokenPanda addon folder with the new version.
4. Replace the old TokenPandaTray executable with the matching current release.
5. Start TokenPandaTray.
6. Review the configured Classic and Retail regions.
7. Synchronize the enabled data sources.
8. Start World of Warcraft.

Do not mix files from different addon versions.

For TokenPanda 1.4.0, modern data is stored in:

```text
Data/<Flavor>/<Region>/HistoricalData.lua
Data/<Flavor>/<Region>/RealmData.lua
```

The root `HistoricalData.lua` exists only for legacy fallback compatibility in the 1.4.0 release line.

---

## Common problems

### The addon does not appear

Avoid a duplicated folder:

```text
Incorrect: AddOns/TokenPanda/TokenPanda/TokenPanda.toc
Correct:   AddOns/TokenPanda/TokenPanda.toc
```

### Locale keys appear on screen

Fully close WoW, replace the complete addon folder, and restart the game.

### The chart does not update

Confirm that TokenPandaTray is synchronizing the correct Flavor and Region.

If Tray still reports that WoW is running after the game closes, restart TokenPandaTray and synchronize again.

### The selected data source resets after /reload

This is expected.

Manual Matchbox 2.0 selections are session-only. TokenPanda returns to the tuple matching the current WoW client after `/reload` or a full restart.

---

## Projection disclaimer

TokenPanda includes approximate value projections intended only to represent a possible trend.

Projected values:

- are not guaranteed future prices;
- can change when new historical samples are received;
- should not be used as the sole basis for a decision.

Every decision must be made under the user's own judgment.

---

## Security and privacy

TokenPandaTray:

- does not request World of Warcraft or Battle.net passwords;
- does not sign in to Battle.net;
- does not modify the World of Warcraft executable;
- does not require an account;
- downloads public data and maintains TokenPanda local data files.

---

## Bug reports

Use the repository's **GitHub Issues** section.

When reporting a synchronization or data issue, include:

- TokenPanda version;
- TokenPandaTray version;
- game Flavor: Classic or Retail;
- selected region;
- whether World of Warcraft was running;
- relevant TokenPandaTray log information when available.

---

## Independent project

TokenPanda is independent and unofficial.

It is not affiliated with, sponsored by, authorized by, or endorsed by Blizzard Entertainment or by the operators of any public data service used by the project.

World of Warcraft, WoW, and Blizzard Entertainment are trademarks or registered trademarks of Blizzard Entertainment, Inc.

---

**EZ-Mouse Dev. — Obsessed with perfection.**
