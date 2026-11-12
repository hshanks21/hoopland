# hoopland

Hoopland Leagues and Files.

## Team logos

`logos/` holds all game artwork, 256×256 PNGs:

- `{shortName}.png` — one per team (e.g. `ALA.png` = Alabama Crimson Tide)
- `NCAA.png` — league logo (stand-in; the original custom "Men's College Basketball" logo is unrecoverable)
- `ALLAMERICAN.png` — McDonald's All-American Game logo (used for both EAST/WEST star teams)
- `manifest.csv` — maps `short → city → name → file`

The `logoURL`, `overlayURL` (court-center logo), and `adsURL` (ad-board logo) fields in `hoopland-data.txt` all point at these files via GitHub's raw CDN:

```
https://raw.githubusercontent.com/hshanks21/hoopland/main/logos/{shortName}.png
```

Because this repo is public, the game fetches the logos directly at import time — no auth needed. If a logo is ever replaced, just overwrite the PNG and the URL stays valid (files are served from `main`).

All logos are official NCAA/university/McDonald's marks sourced from Wikipedia/Wikimedia — for personal/internal use only.
