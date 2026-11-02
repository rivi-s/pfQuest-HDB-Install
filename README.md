# pfQuest-HDB-Install

pfQuest maps, tracker, journal, browser, and gathering tracking with an English SQLite database supplied through HearthDB.

This ready-to-install bundle includes the embedded provider and English SQLite database. The `pfQuest` addon folder is included. The optional Russian pack is distributed separately.

## Choose an edition

| Edition | Install | Requirements |
| --- | --- | --- |
| Regular pfQuest | [pfQuest](https://github.com/rivi-s/pfQuest) | Loads its database in Lua; no HearthDB DLL required. |
| Regular Turtle/Raven content | [pfQuest-turtle](https://github.com/rivi-s/pfQuest-turtle) alongside regular pfQuest | Both regular addon folders. |
| HDB Vanilla | [pfQuest-HDB-Install](https://github.com/rivi-s/pfQuest-HDB-Install) | HearthDB client component; English database included. |
| HDB Turtle/Raven content | [pfQuest-turtle-HDB-Install](https://github.com/rivi-s/pfQuest-turtle-HDB-Install) | HearthDB client component; both addon folders and combined English database included. |

Install one edition at a time. Both editions use the folder names `pfQuest` and `pfQuest-turtle`; mixing regular and HDB folders can leave the wrong database or code loaded.

## Install or update

1. Fully close World of Warcraft. Preserve your `WTF` settings and back up addon folders when switching editions.
2. Download **[this install bundle](https://github.com/rivi-s/pfQuest-HDB-Install/archive/refs/heads/main.zip)** and extract it.
3. Replace `pfQuest` in `Interface/AddOns` with the inner addon folders from this bundle. Remove the old folders first so obsolete files are not left behind.
4. Remove legacy `pfQuest-HearthDB` and `pfQuest-HearthDB-turtle` provider folders. Any small inactive compatibility stubs included in the bundle are migration files, not required providers.
5. Confirm the client has HearthDB support, restart, enable the addons, and run `/pfqhdb` to verify the database opened.

The database belongs at `pfQuest/provider/data/pfquest.sqlite` inside `Interface/AddOns`. For Turtle/Raven custom content, choose the complete Turtle install bundle above.

## DLL and diagnostics

The existing HearthDB DLL remains supported. The [0.4.1-exp.3 DLL](https://github.com/rivi-s/HearthDB/releases/tag/v0.4.1-exp.3) is an optional separate download. This bundle does not install a DLL or plugin loader. Fully exit the game before replacing a DLL; `/reload` cannot replace it. HDB requires the client component and has no Lua database fallback.

The included `pfQuest-HDB-HitchProfiler` is optional. Login capture defaults to off for new installations. Enable the diagnostic addon only when needed; `/hdbhitch on` starts a manual capture and `/hdbhitch off` stops it. See [SUPPORT.md](SUPPORT.md) for login options, manual log paths, troubleshooting, and reporting.

## Project status

Maintenance focuses on occasional database corrections and reported bugs. Updates have no fixed schedule. Compatibility with Raven's Classic Era 1.14 client is unverified; work on that port is paused. These packages target the existing 1.12 client.

## Source and credits

Addon source: [pfQuest-HDB](https://github.com/rivi-s/pfQuest-HDB).

Original pfQuest authors: Shagu and txtsd. Original Turtle extension: Shagu, with contributors listed in the addon TOC. Rivi maintains these forks and contributes features, database corrections, and HearthDB integration.
