# thread-flag-public

Public assets for the [ThreadFlag](https://github.com/hoyaaaa/thread-flag) browser extension.

## Contents

- **`aliases.json`** — Maps unrecognized location strings to ISO 3166-1 alpha-2 country codes
- **`privacy.html`** — [Privacy Policy](https://hoyaaaa.github.io/thread-flag-public/privacy)

## aliases.json

When the extension encounters a location string it cannot match (e.g. a city name like `"seoul"`), it reports the miss to a Cloudflare Worker which auto-resolves via Wikidata and opens a pull request here.

Format:
```json
{
  "location string": "CC"
}
```

- Keys are lowercase, trimmed location strings as they appear on Threads profiles
- Values are ISO 3166-1 alpha-2 country codes (e.g. `"KR"`, `"JP"`)
- Empty string value means the location could not be resolved and needs manual mapping

## Contributing

To add or correct a mapping, open a pull request editing `aliases.json`.
