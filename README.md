# Feat/Non-Confidence Interval Tutorial

This branch adds a new tutorial that shows a warning about the non-confidence interval (8kHz~).

The non-confidence interval is a region considered unreliable due to the nature of IEC 60318-4 (711) measurement equipment. This is also where the over-represented resonance peak of 711 begins.

You can edit this to utilize it as some kind of warning region.

## Usage

Enable or disable this feature in `config.js`.

```js
const enableNonConfidenceIntervalTutorial = true;
```