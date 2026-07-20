# TokenPanda User Guide

## What is TokenPanda?

TokenPanda displays the current WoW Token price and recent price history inside World of Warcraft. **TokenPandaTray** downloads and synchronizes the data used by the addon.

This guide applies to:

```text
TokenPanda 1.0.0 Beta
TokenPandaTray 1.0.0 Beta
```

## Installation

### 1. Install the addon

1. Close World of Warcraft.
2. Extract `TokenPanda-1.0.0-beta.zip`.
3. Copy the `TokenPanda` folder into:

```text
World of Warcraft/_classic_/Interface/AddOns/
```

The final path must be:

```text
Interface/AddOns/TokenPanda/TokenPanda.toc
```

### 2. Start TokenPandaTray

1. Extract `TokenPandaTray-1.0.0-beta.zip`.
2. Run `TokenPandaTray.exe`.
3. Select your WoW Classic folder.
4. Select US, EU, KR, or TW.
5. Enable synchronization.

TokenPandaTray is portable and requires no traditional installation.

## Open TokenPanda

Enter `/tokenpanda` in the game or use the minimap icon.

## Controls

- **Minimap left-click:** show or hide TokenPanda.
- **Minimap right-click:** show or hide the menu.
- **Drag minimap icon:** move it.
- **Minimize button:** compact view.
- **Right-click minimize button:** switch between normal and analysis views.
- Each view keeps its own position.

## Chart

Available periods: `3D · 7D · 14D · 1M · 3M · 6M · ALL`

- Yellow line: current period.
- Red line: previous equivalent period.

## “No history”

1. Check that TokenPandaTray is running.
2. Confirm synchronization is enabled.
3. Verify the WoW folder and region.
4. Wait for the first synchronization.
5. Use `/reload` if WoW was already open.

## Updating

1. Fully close WoW and TokenPandaTray.
2. Replace the old addon folder with the new one.
3. Keep `HistoricalData.lua` only when release notes confirm compatibility.
4. Start TokenPandaTray, then WoW.

Do not mix files from different versions.

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

Confirm that TokenPandaTray is synchronizing the correct region.

## Security and privacy

TokenPandaTray does not request passwords, sign in to Battle.net, or modify the game executable. It only downloads public data and updates the addon's local data file.

## Bug reports

Use the repository's **GitHub Issues** section.

**EZ-Mouse Dev. — Obsessed with perfection.**
