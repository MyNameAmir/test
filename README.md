# FIFA World Cup 2026 — Interactive 3D Globe

A single-file, interactive 3D globe of Earth (inspired by [Globle](https://globle-game.com/))
that highlights every nation in the FIFA World Cup 2026.

## What you see

- Every country in the world is drawn with **white borders**.
- Countries **not** in the tournament are **grey**.
- **Qualified nations** are coloured a **coppery orange**.
- **Host nations** are coloured separately: **USA → blue**, **Canada → red**, **Mexico → red**.
- **Hovering** a World Cup nation pops up a box with that nation's **flag** and a **fun fact**.
  Non-tournament countries show no tooltip.

## Running it

It's a fully self-contained `index.html`. Just open it in any modern browser, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

An internet connection is required the first time so the page can load:

- the globe engine ([globe.gl](https://github.com/vasturiano/globe.gl) / three.js, via unpkg CDN),
- country shapes (Natural Earth 1:50m GeoJSON), and
- flag images (flagcdn.com).

## Notes

- "England" is matched to the United Kingdom polygon (`GB`) since standard country
  datasets don't split the UK into its home nations; its tooltip uses the England flag.
- The set of 48 nations is encoded in the `WC2026` object near the top of the script —
  edit names, colours or facts there to customise the map.
