# gourusumathi.github.io

Site for **Sumam Prathi Sumam** (సుమం ప్రతి సుమం) — Gouru Sumathi's YouTube channel from Warangal district, Telangana: farming, cooking, gardening, travel and craft.

Channel: <https://www.youtube.com/@sumamprathisumam>

Static, single page, no build step and no dependencies. Fonts load from Google Fonts; the portrait is embedded in `index.html` as a data URI, so `index.html` works on its own even if nothing else is uploaded.

## Files

| Path | What it is |
| --- | --- |
| `index.html` | The whole site — markup, CSS and a small reveal-on-scroll script |
| `assets/sumathi.jpg` | The portrait at 820px wide, kept for reuse (social cards, future pages) |

## Publishing on GitHub Pages

The repository name must match the account name exactly: account `gourusumathi` → repository `gourusumathi.github.io`.

1. Create the empty repository on GitHub (no README, no .gitignore — this folder already has them).
2. Push:

   ```bash
   git remote add origin https://github.com/gourusumathi/gourusumathi.github.io.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Build and deployment**, source *Deploy from a branch*, branch `main`, folder `/ (root)`.

The site goes live at `https://gourusumathi.github.io` within a few minutes.

## Editing

Everything lives in `index.html`.

- **Colours** — the `:root` block at the top: indigo `#16233D`, oxblood `#6B1E2A`, zari gold `#C9992F`, ivory `#EFEAE1`.
- **Recipes** — the `<article class="dish">` blocks in the "From the kitchen" section.
- **Sandalwood planting date** — the `PLANTED` constant in the script at the bottom of the file. The grove's age on the page is calculated from it, so it stays correct forever without editing. `HARVEST_YEARS` sets the countdown target.
- **Grove stages** — the `<li class="stage">` items. Add the class `done` to a stage once it has passed; the marker fills in.
- **Monthly farm update** — the `<div class="row">` lines under "On the land right now".
- **Links** — the YouTube handle appears twice (hero button and footer); Instagram and email are in the footer.

## Still to fill in

- Sandalwood planting date — currently July 2019, a placeholder
- Instagram URL (currently a bare link — remove the line if there is no account)
- Contact address (currently `hello@example.com`)
