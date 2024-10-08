# Feat/l10n (Localization)

This branch adds a new localization feature to the graphtool.

- Add new Language Selector to the top right corner.
- Add new 'translate.js' to handle language files.
- Add new 'assets/lang' directory to store language files.
- Slightly adjusts the layout of the graphtool to fit the new features.

## Usage

Enable or disable features in `config.js`.

```js
// Allow the creator to have a button top right to support them
allowLanguageSelector = true; 

// List of available language codes. When you are adding a new language, make sure to use ISO 639-1 Language Codes for auto-detection.
availableLanguages = ["en", "ko"]; 

// Determine default language based on user's browser
// You don't need to change this - unless you are setting fallback language from "en" to something else.
defaultLanguage = (function () {
  const browserLang = navigator.language.split("-")[0];
  return availableLanguages.includes(browserLang) ? browserLang : "en";
})(); 

// If true, translated header link from language files will be used over the one from config.js
// If false, the header data from config.js will be used.
translateHeader = true; 

// If true, translated tutorial from language files will be used over the one from config.js
// If false, the tutorial data from config.js will be used.
translateTutorial = true; 

// If true, translated accessories from language files will be used over the one from config.js
// If false, the accessories data from config.js will be used.
translateAccessories = true; 
```

## Adding New Language

To make sure your language is automatically detected by the browser, you need to find out the ISO 639-1 language code of your language.

- [ISO 639-1 Language Codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)

Please refer to the link above for more information.

1. Add new language code to `config.js`
```js
availableLanguages = ["en", "ko"]; 
```

2. Add new .JSON language file to `assets/lang/`
```
/assets/lang/
- en.json
- ko.json
```

3. Edit the .JSON language file with the language you want to add.
```json
{
  "header": {
    "logoText": "Your Name",
    "links": [
      {
        "name": "Your Link Name",
        "url": "Your Link URL"
      },
      ...
    ]
  },
  "tutorial": [
    {
      "name": "Your Tutorial Name",
      "width": "Your Tutorial Width",
      "description": "Your Tutorial Description"
    },
    ...
  ],
  "accessories": {
    "content": "Your Accessories Content"
  },
  "main": {
    ...
  }
}
```
Please refer to `assets/lang/ko.json` if you need more examples.
