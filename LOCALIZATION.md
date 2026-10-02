# Localization structure

The site uses two real language files:

- `lang/en.js` — English
- `lang/ru.js` — Russian

Teyvat Script is **not** a language file. It is a script/display mode that renders the English localization through the Teyvat font.

## Add or edit text

HTML elements use a localization key:

```html
<p data-l10n="archive.exampleText">English fallback text</p>
```

Add the same key to both language files:

```js
// lang/en.js
"archive.exampleText": "English text"

// lang/ru.js
"archive.exampleText": "Русский текст"
```

For image alt text use `data-l10n-alt="key"`.

Dynamic Segment and media text is also stored in these language files. `data.js` keeps non-language data such as image data, video IDs, years, and localization-key references.

Because the language files are ordinary JavaScript loaded before `script.js`, this structure also works when the project is opened locally from files and does not depend on `fetch()` or a server.
