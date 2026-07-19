# RustCalc

[![Latest release](https://img.shields.io/github/v/release/Bray12541/Rust-Calculator?display_name=tag&sort=semver)](https://github.com/Bray12541/Rust-Calculator/releases/latest)
[![Windows](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011-1674d1)](https://github.com/Bray12541/Rust-Calculator/releases/latest)
[![Unofficial Rust companion](https://img.shields.io/badge/Rust-unofficial%20companion-dc513a)](#disclaimer)

RustCalc is a fast, offline-first Windows companion for **Rust** raid planning,
crafting, and recycling. Search the complete item database, calculate a raid
path, account for damaged walls or doors, and share the finished plan without
opening a browser for every calculation.

![RustCalc raid planner](screenshots/raid-planner.png)

## Download

Download the installer from the **[latest RustCalc release](https://github.com/Bray12541/Rust-Calculator/releases/latest)**.

1. Download `RustCalc-Setup-2.3.0.exe` from the release's **Assets** section.
2. Run the installer.
3. Launch RustCalc from the desktop shortcut or Start Menu.

Python is not required. RustCalc supports 64-bit Windows 10 and Windows 11.

> RustCalc is currently unsigned. Microsoft Defender SmartScreen may identify
> a newly downloaded build as an unrecognized application. Verify that the
> installer came from this repository and that its checksum matches the value
> below before selecting **More info → Run anyway**.

## Features

### Raid costs and planning

- Searchable raid costs for building pieces, doors, deployables, and other targets
- One clear result per ammunition or attack type
- Responsive Tool, Damage, Quantity, Time, Fuel, HQM, and Sulfur columns
- Multi-target raid plans with combined ammunition, sulfur, and time totals
- Partial-health calculations for damaged walls and doors
- Remaining HP and overkill shown for each damage method
- Persistent plans, favorites, recent items, and reusable presets

### Stockpile and farming

- Enter crafted explosives and raw materials already in your stockpile
- Build mixed-method raid loadouts that reduce overkill and material waste
- Compare Cheapest Sulfur, Fastest Raid, Eco Raid, No Workbench 3, and Best Stockpile Fit recommendations
- See the exact amount still required after subtracting owned items
- Estimate sulfur nodes, ore, furnace loads, charcoal, wood, smelting time, and crafting time
- Configure Small, Large, or Electric Furnaces and the number running in parallel

### Crafting and recycling

- Complete searchable crafting and recycling databases
- Quantity calculator for crafting batches and total materials
- Raw-material expansion for craftable components
- Radtown and safe-zone recycler estimates

### Export and sharing

- Copy formatted raid plans to the clipboard
- Discord-friendly output
- Save a raid plan as a PNG image
- Import and export saved plans as JSON

### Updates and diagnostics

- Automatic application updates using a dedicated updater executable
- Automatic official Rust changelist detection and independent game-data updates
- Fast compressed data packages instead of hundreds of individual page requests
- SHA-256 verification, previous-data rollback, retry cooldowns, and update history
- Offline item icons bundled with the application
- On-demand icon downloads for newly added Rust items
- Lazy-loaded icons that continue appearing as long raid tables are scrolled
- Settings for update preferences, UI scale, text size, and window position
- Crash logs, diagnostics, update history, and raid-data regression checks

![RustCalc crafting calculator](screenshots/crafting.png)

## Automatic updates

RustCalc can update an existing installation. When a newer verified GitHub
release is available, the application downloads its installer, closes safely,
runs the dedicated updater, and relaunches the updated version. Users do not
need to uninstall RustCalc or manually replace application files.

Application and game-data update checks can be enabled or disabled from
**Settings**. Game data has its own small update channel, independent of app
releases, and can also detect new item identities from the live catalogue after
an official Rust patch. Packages are verified with SHA-256 and regression-tested
before activation; the previous working data remains available for rollback.
Saved raid plans and preferences are retained during application updates.

## Verify the installer

RustCalc v2.3.0 installer SHA-256:

```text
5A7B85733E97C1B4E03EAB102CB885DC43FA6F3491948D03573F04E66C6B868B
```

In PowerShell, verify a downloaded installer with:

```powershell
Get-FileHash .\RustCalc-Setup-2.3.0.exe -Algorithm SHA256
```

The resulting hash should exactly match the value above.

## Data and privacy

RustCalc stores settings, downloaded game data, saved plans, and crash logs
locally under `%LOCALAPPDATA%\RustCalc`. It does not require an account and does
not upload saved plans or diagnostics. Internet access is used only for update
checks and downloading updated application or game data.

Raid and item information can change after Rust patches. Use **Update Data** in
RustCalc to retrieve the newest supported dataset. Each downloaded raid target
is automatically validated before replacing the working offline data.

## Current version

**RustCalc 2.3.0**

See the [GitHub Releases page](https://github.com/Bray12541/Rust-Calculator/releases)
for release notes and previous installers.

## Disclaimer

**RustCalc is an unofficial Rust companion and is not affiliated with,
endorsed by, or sponsored by Facepunch Studios.** Rust and related trademarks,
game data, and game assets belong to their respective owners.
