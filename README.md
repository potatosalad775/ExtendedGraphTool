# PublicGraphTool for Squig.link

This version of PublicGraphTool has been modified to be compatible with Squig.link. \
Simply [download all files from here](https://github.com/potatosalad775/ExtendedGraphTool/archive/refs/heads/squiglink.zip), and replace your squig.link database with this one.

It is **highly recommended** to manually move the data files and edit new config.js to your liking. (**Do not overwrite** with old files) \
Be sure to make a backup before proceeding.

If you are having trouble migrating your database, please contact potatosalad775@discord for assistance.

## Migration Tutorial

```
1. Download this PublicGraphTool and your own existing squig.link database into separate folders on your computer.

2. Move the files that don't need any changes

- Measurement data files (.txt) -> /data/zero2.txt
- phone_book.json -> /data/phone_book.json
- Image files -> /assets/images/sample.img

3. Edit several files that need to be modified

- config.js
  - Carefully migrate your previous changes to the new config.js.
  - Be careful with the directories. Take note of what's already documented in there and modify it accordingly.

- index.html
  - Everything inside the <head> tag is safe to edit.
  - Be careful not to accidentally remove or edit scripts inside the <body> tag.

4. (Optional) Personalize addon features

- Localization
  - You can add support for foreign languages. Please see `/assets/lang/en.json` and `/assets/lang/ko.json` for more information.

5. Move new GraphTool to live server

- Access your own database with an FTP client, create a new directory (e.g. '_backup') and move whole existing files into it.
- Move your new GraphTool files to the database server and you should be ready to go.
```

## Changes from Original PublicGraphTool

- Modified data folder structure
  - headphones measurement data are now located in a separate headphones folder.
- Applied Squig.link's graphAnalytics script
- Added listAugment.js
- Added squig.link features

---


# PublicGraphTool Demo Page
https://graphtool-demo.harutohiroki.com/

## Changes
- Added Equalizer (cred to Rohsa)
- Added Uploads
- Added Targets
- Added Website link on graph (cred to MRS)
- Re-themed graph window
- Re-done Frequency Range definitions
- Changed parser to universal parser
- Removed Restricted mode (cuz I want to keep it free)
- Reorganised code
- Moved targets to a different folder for organization
- Moved phone_book outside for easier access
- Added a function to average all active graphs (requested by listener)
- Custom Diffuse Field Tilt (requested by listener)
- Restyled EQ tab
- EQable pink noise in EQ tab (requested by listener)
- Added the ability to upload your own test track to EQ (requested by rollo)
- Added a button to disable and enable all EQ bands (requested by SK)
- Tone generator now EQable (requested by SK)
- Added a Channel balance slider
- Added a song progress slider to the EQ demo section (requested by XiaoShe)
- Added Ear Gain customisation to custom tilt (requested by listener)
- Made any target tiltable (requested by listener)
- Added Treble customisation to custom tilt (requested by listener)
- Added a button to swap between different y-axis scales (requested by rollo)
- Added Preference Bounds and Preference Bound scaling (requested by listener)
- Reversed the "any target tiltable" feature, now applying tilt on target automatically if supported (requested by listener)
- Per-measurement compensation (requested by listener)
- Added support for Haruto's Graph Extension to apply eq to browserwide 
- Made Preference Bounds better and not relying on a png anymore
- Downloadable CSV of all active graphs
- Per page Y scaling (requested by listener)
- Added a Graph Customisation menu


## TODO
- Implement a way to measure the SPL of an IEM and decide whether to upload it or not, skipping REW
  - ability to select which mic/output to use
  - ability to select calibration files
  - ability to apply smoothing
- Trace Arithmetic
- Realtime Analysis

## P.S.
- If you do implement code in here, do leave credits to the original author (me) and the contributors (Rohsa, MRS)
