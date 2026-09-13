# Empower Compass · Democrats Empower Medina

Volunteer companion app for DEM: election dates and deadlines, representative
cards with tap-to-call across Wadsworth / Brunswick / Medina, events with
recurrence and .ics export, canvass sessions with big counters and shareable
summaries, editable scripts, a voting plan builder, and a personal action log.
All data lives on the device; backup/restore under More.

## Files
- `index.html` — the entire app (EM 1.2)
- `sw.js` — offline cache. **CACHE name must match the app version on every deploy.**
- `manifest.json`, `icon-192.png`, `icon-512.png` — PWA install
- `HOW-TO-UPDATE-CITIES.md` — plain-English guide for updating officials

## Update ritual (every change)
1. Bump `VERSION` in `index.html` (stamp the REAL current date).
2. Bump `CACHE` in `sw.js` to match.
3. Commit both together.

## Data refresh after Nov 3, 2026
Update `KEY_DATES`, `ELECTION_DAY`, `DATA_VERIFIED`, and confirm officials in
`CITIES` and `SHARED_SECTIONS` — all near the top of `index.html`.
