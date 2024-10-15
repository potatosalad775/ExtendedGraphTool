# Feat/l10n (Localization)

## Important Notice

This feature has been included to [Original PublicGraphTool project by HarutoHiroki](https://github.com/HarutoHiroki/PublicGraphTool/pull/2). \
You don't need to manually pull or fetch to apply this feature.

---

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

// List of available language codes. 
// When you are adding a new language, make sure to use ISO 639-1 Language Codes for auto-detection.
availableLanguages = ["en", "ko"]; 

// Determine default (fallback) language. It should be included in the availableLanguages list.
defaultLanguage = "en";          

// If true, the browser's language will be used as the default language. 
// If false, the defaultLanguage setting will be used as the default.
useBrowserLangAsDefault = true; 

// If true, translated header link from language files will be used over the one from config.js
// If false, the header data from config.js will be used.
translateHeader = true; 

// If true, translated tutorial from language files will be used over the one from config.js
// If false, the tutorial data from config.js will be used.
translateTutorial = true; 

// If true, translated accessories from language files will be used over the one from config.js
// If false, the accessories data from config.js will be used.
translateAccessories = true; 

// If true, translated target types from language files will be used over the one from config.js
// If false, the target types data from config.js will be used.
translateTargetTypes = true;

// If true, translated alert messages from language files will be used.
translateAlertMessages = true;
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
  },
  "alertMessages": {
    ...
  }
}
```
Please refer to `assets/lang/ko.json` if you need more examples.

## Things to Note

When you are modifying the name of the objects in `config.js`, you need to edit `translate.js` accordingly.

```js
// For example, if you really need to modify the name of the Accessories content from 'simpleAbout' to 'whateverAbout'...

async function loadTranslations(lang) {

  // ...

  if(lang == "en") {
    // ... 
    whichAccessoriesToUse = whateverAbout; // This line needs to be modified.
  }
  else {
    // ... 
    if (translateAccessories) {
      whichAccessoriesToUse = translations.accessories.content || whateverAbout; // This line also needs to be modified.
    }
  }

  // ...
}

// These changes will make sure the new name is reflected in the graphtool.
```
