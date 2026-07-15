# TICO Assets Downloader

App that automatically finds, downloads, converts, and organizes covers, backgrounds, icons, and logos for your TICO game library—without any headaches.

![TICO Assets Downloader main window](main-window.png)

## Features

- Downloads covers, backgrounds, icons, and transparent logos
- Processes your entire library, selected systems, or specific games
- Detects existing artwork and downloads only missing assets
- Optionally replaces and refreshes older artwork
- Includes a safe preview mode that scans without downloading
- Displays live progress, download statistics, and artwork previews
- Shows game counts for individual or combined systems
- Generates a missing-assets report when artwork cannot be found
- Resolves short FBNeo filenames automatically

## Artwork providers

The app searches SteamGridDB first using multiple title and artwork variations. If an asset is unavailable, it automatically checks Libretro thumbnail repositories, the REG-Vault community API, and Wikimedia Commons.

Only a free SteamGridDB API key is required. It is used for the current session and is never saved by the application.

## Screenshots

### Library game counts

![Library game counts](library-counts.png)

### Select specific games

![Specific game selection and artwork status](game-selection.png)

## Supported assets

| Asset | Output format |
| --- | --- |
| Covers | 512 × 512 JPG |
| Backgrounds | 1920 × 620 JPG |
| Icons | 256 × 256 PNG |
| Logos | Transparent PNG |

Downloaded artwork is automatically converted, named to match the game file, and saved in the correct TICO asset folder.

## Requirements

- Windows 10 or Windows 11, 64-bit
- Internet connection
- Free [SteamGridDB API key](https://www.steamgriddb.com/profile/preferences/api)

The packaged application is standalone. PowerShell, Python, and a separate .NET installation are not required.

## Quick start

1. Download the ZIP from the [latest release](../../releases/latest).
2. Extract the ZIP file.
3. Run `TICO ASSETS DOWNLOADER by TCJ.exe`.
4. Enter your SteamGridDB API key.
5. Select your main TICO folder.
6. Choose the desired artwork and systems.
7. Use **Preview only** for a safe first scan, or select **Download Assets**.

Existing artwork is skipped automatically unless **Replace and update old assets** is enabled.

## Missing artwork

If artwork is still unavailable after every provider has been checked, the app creates `TICO Missing Assets.txt` in the main TICO folder. The report lists the system, original filename, resolved game title, and missing asset types.

## Disclaimer

This is an unofficial community tool and is not affiliated with SteamGridDB or the TICO project.

Artwork availability and usage rights vary by provider. Review the relevant source licensing before redistributing downloaded images.
