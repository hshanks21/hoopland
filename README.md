# hoopland

Hoopland Leagues and Files.

## Team logos

`logos/` holds the 64 team logos + the league logo, all 256×256 PNGs:

- `{shortName}.png` — one per team (e.g. `ALA.png` = Alabama Crimson Tide)
- `NCAA.png` — league logo (stand-in; the original custom "Men's College Basketball" logo is unrecoverable)
- `manifest.csv` — maps `short → city → name → file`

The `logoURL` fields in `hoopland-data.txt` point at these files via GitHub's raw CDN:

```
https://raw.githubusercontent.com/hshanks21/hoopland/main/logos/{shortName}.png
```

Because this repo is public, the game can fetch the logos directly at import time — no auth needed. If a logo is ever replaced, just overwrite the PNG and the URL stays valid (files are served from `main`).

Logos are official NCAA/university marks sourced from Wikipedia/Wikimedia — for personal/internal use only.

## Known gaps

- The two All-American (McDonald's) star-team logos share one `logoURL` that is still a dead Dropbox link — no replacement has been sourced yet.
- `overlayURL` (court overlays) and `adsURL` (advertisements) in `hoopland-data.txt` still point at dead Dropbox links. These are not team logos and were left as-is.
