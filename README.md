# TICO Assets Downloader

Transform your TICO game library in minutes. This standalone Windows app automatically finds, downloads, converts, and organizes covers, backgrounds, icons, and logos for every game—saving them directly to your TICO folder and eliminating countless hours of tedious manual downloads on your Switch.

<img width="1348" height="745" alt="image" src="https://github.com/user-attachments/assets/4a7c19b4-aa0f-4fbb-b9e1-21c218645346" />

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

<img width="655" height="437" alt="image" src="https://github.com/user-attachments/assets/df2012ae-777b-45e0-983a-4f4965ab79ba" />

### Select specific games

<img width="972" height="757" alt="image" src="https://github.com/user-attachments/assets/b8011f3d-9126-474e-adc4-550d792012da" />

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
