# CrypTrack

A dark-themed global cryptid sightings atlas. Three plain files, no
build step — open `index.html` (or serve the folder) and it runs.

| File           | Role |
| -------------- | ---- |
| `index.html`   | Markup + script/style includes |
| `style.css`    | All styling |
| `bigfoot.js`   | Data, map, charts, UI wiring |

## What's in it

- **Leaflet** dark CartoDB tiles with marker clustering
- **Live BFRO feed** — ~5,000 geocoded Sasquatch reports via the
  `timothyrenner/bigfoot-dash-app` mirror (CSV → PapaParse Web Worker)
- **Live NUFORC feed** — ~80,000 geocoded UFO/UAP reports from
  `planetsig/ufo-reports` (geolocated NUFORC archive)
- **Curated global cryptid layer** — 25+ hand-written entries with
  Wikipedia links (Yeti, Yowie, Yeren, Almas, Orang Pendek, Mapinguari,
  Hibagon, Mande Barung, Patterson–Gimlin, Skookum cast, Ape Canyon, …)
- **Hover cards** with class, date, season, location, summary and quick
  Wikipedia / source links
- **Detail modal** on click with weather conditions / UAP shape +
  duration and reference links
- **Filters** — BFRO classification (A/B/C), UAP, global, season, year
  range, free-text search across title/state/county/description
- **Chart.js trend panels** — sightings by decade, by season, top states
- **Version chip** — click for in-app patch notes and feed status
- **Scanner FX** — animated grid, scanlines, radar loader, pulse markers

## Data sources (all free, public)

- BFRO geocoded reports — public dataset by Timothy Renner
- NUFORC geolocated/standardized archive — `planetsig/ufo-reports`
- CartoDB Dark Matter map tiles — free for OSM-attributed use
- Wikipedia article links per cryptid
- BFRO and NUFORC public report URLs

## Notes

- No API key required.
- CSVs parse in a Web Worker so the UI stays responsive on initial load.
- If both jsDelivr and raw.githubusercontent.com block a fetch, the feed
  status shows `offline` and the remaining layers keep working.
