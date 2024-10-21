# ExtendedGraphTool

This repo is a fork of [PublicGraphTool](https://github.com/HarutoHiroki/PublicGraphTool) with additional features and modifications.

Are you looking for a 'squig.link compatible' PublicGraphTool? Head over to ['squiglink' branch](https://github.com/potatosalad775/ExtendedGraphTool/tree/squiglink).

## Demo Page
N/A yet, but you can see my squig.link [here](https://silicagel.squig.link) atm.

## Additional Features

Each additional features are implemented in a separate branch. \
You can checkout to each branch to see or implement those features.

The 'custom' branch includes all additional features mentioned below.

### Multi-language Support - [(branch)](https://github.com/potatosalad775/ExtendedGraphTool/tree/feat/l10n)

Adds Multi-Language Support to GraphTool.

*This feature has now been implemented to [the OG PublicGraphTool.](https://github.com/HarutoHiroki/PublicGraphTool/pull/2)*

### Non-Confidence Interval Tutorial - [(branch)](https://github.com/potatosalad775/ExtendedGraphTool/tree/feat/Non-Confidence-Interval-Tutorial)

Adds a Tutorial on the Non-Confidence Interval of IEC 60318-4 compliant ear simulators. (8kHz~)

---

# PublicGraphTool by mlochbaum (HarutoHiroki)

## Changes
- Added Equalizer (cred to Rohsa)
- Added Upload
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
- Added Translations (Thanks to potatosalad775)
- Brought the public version up to date

## TODO
- Implement a way to measure the SPL of an IEM and decide whether to upload it or not, skipping REW
  - ability to select which mic/output to use
  - ability to select calibration files
  - ability to apply smoothing
- Trace Arithmetic
- Realtime Analysis
- 
## For Contributors
- The code is a mess, I know. I'm working on it. I'm sorry.
- If you want to contribute and help translate the tool, all the source English text is in the `en.json` file. Just copy the file and rename it to your language code (make sure to use ISO 639-1 Language Codes for auto-detection e.g. `fr.json` for French) and translate the text. I'll take care of the rest.
- The translation feature will always prioritize what's in the language files. If a text is missing in the translation file, it will default to the text in the `config.json` file.
- Please don't make any text/value `null`. If you want to not have a text/value, just leave it empty (e.g. `""` or `[]`).
- For targets, each target `"type"` is a key in the language files. The value of the key is the name of the category of targets.

## P.S.
- If you do implement code in here, do leave credits to the original author (me) and the contributors (Rohsa, MRS, potatosalad775)