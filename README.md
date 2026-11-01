# CPAP Ledger

A single-page web app for reading the SD card from a ResMed AirSense 10 CPAP machine.

- **Report**: a plain-English report card for the last 30 or 90 days (nights used, hours per night, AHI, mask seal, bedtime routine).
- **Charts**: nightly use, AHI and leak over 30 days, 90 days, a year or everything.
- **Night**: a zoomable, time-aligned strip chart of flow, pressure, leak, respiratory rate, tidal volume, minute ventilation, snore and flow limitation, with apnea and hypopnea events marked.
- **Import**: pick `STR.edf` and files from `DATALOG` (or the whole SD card folder), or load a backup `.json` of nightly summaries when the SD card isn't handy.

## Running it

Open `index.html` in a browser. There is no build step and no server.

To host it, turn on GitHub Pages for this repo (Settings → Pages → deploy from the `main` branch, root folder).

## Privacy

Everything is parsed on your device. Imported data is saved in the browser's IndexedDB and is never uploaded. When the page runs as a claude.ai artifact, it can also keep the nightly summaries in that artifact's private storage. Outside claude.ai that step is skipped.

## Disclaimer

For personal viewing only. This is not a medical device and not medical advice. Check anything that worries you against ResMed's own reports or with your care team before changing therapy.
