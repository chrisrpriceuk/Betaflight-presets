# Betaflight Presets

Custom Betaflight preset source for personal presets in the Configurator Presets tab.

## Preset Source Setup

In Betaflight Configurator:

- Go to `Presets` -> `Preset Sources`
- URL: `https://github.com/chrisrpriceuk/Betaflight-presets`
- Branch: `main`

## Included Presets

- `presets/4.5/osd/Chris_osd_4_5_2.txt`
- `presets/4.5/rates/Chris_rates_rp1_4_5_2.txt`
- `presets/4.5/tune/brawler_tune_profile2_exact_4_5_2.txt`

## Update Workflow

When you add or edit any file in `presets/`, regenerate index files before pushing:

```bash
node indexer/indexer.js
node indexer/check.js
```

Then commit and push:

```bash
git add presets index.json index_hash.txt
git commit -m "Update Betaflight presets"
git push
```
