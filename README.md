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

1. Download `RustCalc-Setup-2.1.2.exe` from the release's **Assets** section.
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
- Automatic game-data updates after major Rust patches
- Fast compressed data packages instead of hundreds of individual page requests
- Offline item icons bundled with the application
- Settings for update preferences, UI scale, text size, and window position
- Crash logs, diagnostics, update history, and raid-data regression checks

![RustCalc crafting calculator](screenshots/crafting.png)

## Automatic updates

RustCalc can update an existing installation. When a newer verified GitHub
release is available, the application downloads its installer, closes safely,
runs the dedicated updater, and relaunches the updated version. Users do not
need to uninstall RustCalc or manually replace application files.

Application and game-data update checks can be enabled or disabled from
**Settings**. Game data is distributed as a small compressed release asset,
verified with SHA-256, and regression-tested before activation. Saved raid plans
and preferences are retained during application updates.

## Verify the installer

RustCalc v2.1.2 installer SHA-256:

```text
44EB0B3D62FC07C1BB2D44472D219E59B464238AC33DEA851FD314EADFF244F3
```

In PowerShell, verify a downloaded installer with:

```powershell
Get-FileHash .\RustCalc-Setup-2.1.2.exe -Algorithm SHA256
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

**RustCalc 2.1.2**

See the [GitHub Releases page](https://github.com/Bray12541/Rust-Calculator/releases)
for release notes and previous installers.

## Disclaimer

**RustCalc is an unofficial Rust companion and is not affiliated with,
endorsed by, or sponsored by Facepunch Studios.** Rust and related trademarks,
game data, and game assets belong to their respective owners.
