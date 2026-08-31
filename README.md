# Empower Compass · Democrats Empower Medina

Branded fork of Civic Compass for DEM volunteers: election dates and deadlines,
representative cards with tap-to-call, events with recurrence and .ics export,
canvass sessions with big counters and shareable summaries, editable scripts,
a voting plan builder, and a personal action log. All data lives on the device;
backup/restore under More.

## Files
- `index.html` — the entire app (EM 1.0)
- `sw.js` — offline cache. **CACHE name must match the app version on every deploy.**
- `manifest.json`, `icon-192.png`, `icon-512.png` — PWA install

## Deploy (assumed home)
Repo `empower-compass` → GitHub Pages → https://motbuchanan.github.io/empower-compass/
The Share-app QR inside the app points at that URL. If the org hosts it
elsewhere or on their own domain later, regenerate the QR and update APP_URL
in index.html.

## Fork notes
- localStorage keys are namespaced `em_v1_*` so this app and the public
  Civic Compass never share data on the same origin.
- Scripts, reps, events are all editable in-app — the org maintains its own
  content. Data refreshes after Nov 3, 2026: KEY_DATES, ELECTION_DAY,
  DATA_VERIFIED, and defaultReps() in index.html.
- The public Civic Compass (motbuchanan.github.io/civic-compass/) remains a
  separate, unbranded deployment. Ship changes to each independently.

## Update ritual (every change)
1. Bump `VERSION` in `index.html`.
2. Bump `CACHE` in `sw.js` to match.
3. Commit both together.
