# G-Directory Language Packs

Downloadable translation packs for [G-Directory](https://github.com/synodontis/GK-Software).
The app itself ships with English and French built in; other languages are fetched from
this repo on demand (View > Language > Download More Languages...) and cached locally.

## Structure

- `manifest.json` — the list of available packs: `[{ "code": "es", "name": "Español" }, ...]`
- `<code>.json` — the translation strings for that locale, matching the same key structure
  as the app's own bundled `en.json`/`fr.json` (see the main repo's
  `src/renderer/src/locales/` for the reference structure and full key list)

## Adding a new language

1. Copy `src/renderer/src/locales/en.json` from the main repo as a starting point
2. Translate every value, keeping all keys identical
3. Save it here as `<locale-code>.json` (e.g. `de.json` for German)
4. Add an entry to `manifest.json`
5. Commit and push — no app update needed, it's available to download immediately
