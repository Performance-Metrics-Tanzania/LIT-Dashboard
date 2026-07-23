<<<<<<< HEAD
# LIT Tanzania — Overlap Dashboard

A single-file interactive dashboard showing where four partners (Educate!, TEN/MET, TeachUNITED, ACSL/VVOB) operate across Tanzania: a regional map, scorecards, partner reach, shared-school overlaps and stakeholder engagement.

The whole dashboard is contained in **`index.html`** — the map boundaries, all data, and the D3 library are embedded inside it. There is no build step and no external dependency, so it runs by simply opening the file, and hosts on GitHub Pages as-is.

## Host it on GitHub Pages

1. Create a new repository on GitHub (e.g. `lit-tanzania-dashboard`). Public repos get Pages for free.
2. Upload **`index.html`** to the root of the repository (either drag-and-drop via *Add file → Upload files*, or push with git).
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Set the branch to **`main`** and the folder to **`/ (root)`**, then **Save**.
6. Wait about a minute. Your dashboard will be live at:
   `https://<your-username>.github.io/<repository-name>/`

Because the file is named `index.html`, GitHub Pages serves it automatically at that URL.

### Using git from the command line (optional)

```bash
git init
git add index.html README.md
git commit -m "Add LIT Tanzania overlap dashboard"
git branch -M main
git remote add origin https://github.com/<your-username>/<repository-name>.git
git push -u origin main
```

Then enable Pages as in steps 3–6 above.

## Updating the data later

The data is embedded directly in `index.html` (in two JavaScript variables near the bottom: `GEO` for the map boundaries and `DATA` for everything else). To refresh figures, regenerate the file from the source workbook and replace `index.html` in the repo — Pages redeploys automatically on each push.

## Notes

- Works in any modern browser; no internet connection is required once the page has loaded (D3 is embedded).
- The four Zanzibar regions with no programme data appear amber ("not in programme"); the teal shades show 1, 2 and 3 partners.
=======
# LIT Dashboard Test

This folder includes:

- `index.html` — a static dashboard page that loads `LIT schools summary.xlsx`
- `LIT schools summary.xlsx` — the workbook used as the data source

## How it works

The page uses SheetJS in the browser to fetch and parse the workbook file from the same folder.

## Hosting on GitHub Pages

1. Create a GitHub repository and push this folder to it.
2. Make sure `index.html` and `LIT schools summary.xlsx` are committed.
3. In the repository settings, enable GitHub Pages using the `main` branch and the root folder.
4. Visit the published URL, for example:
   - `https://<username>.github.io/<repository-name>/`

The dashboard will then load the workbook data directly from the repo.

## Notes

- If you use GitHub Pages, the browser can fetch `LIT schools summary.xlsx` from the same site.
- If you open `index.html` locally via `file:///`, the workbook fetch may fail due to browser local file restrictions. Use GitHub Pages or a local HTTP server instead.
>>>>>>> 5da90cb (Add index.html, README and workbook for dashboard)
