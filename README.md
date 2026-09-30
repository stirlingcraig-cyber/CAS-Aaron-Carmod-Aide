# Clydeside Redline

Hot hatch and sports car tuning guide for Glasgow and the west of Scotland.

- 15 cars with 30 UK model-year variants (specs, stage 1/2 estimates, watch items)
- Remap options and per-car tuning platforms
- 52 modifications rated for difficulty, cost, gain, MOT and legal status
- Build planner with cost, power, insurance and legality checks (saved in the browser)
- Glasgow LEZ checker, window-tint checker, Scottish law notes
- Trustpilot-screened garage list (checked 30 September 2026)

It's a single static page (`index.html`) with no build step. Fonts load from Google Fonts; everything else is inline.

## Deploy on GitHub Pages

1. Create a new repository on GitHub (e.g. `clydeside-redline`).
2. Upload the contents of this folder, including the hidden `.github` folder and `.nojekyll`, or push it:
   ```bash
   git init
   git add .
   git commit -m "Clydeside Redline"
   git branch -M main
   git remote add origin https://github.com/<your-username>/clydeside-redline.git
   git push -u origin main
   ```
3. In the repo go to **Settings → Pages → Build and deployment** and set **Source** to **GitHub Actions**.
4. The included workflow deploys on every push to `main`. The site appears at
   `https://<your-username>.github.io/clydeside-redline/`.

No Actions? Set **Source** to **Deploy from a branch**, choose `main` and `/ (root)` instead.

## Run locally

Open `index.html` in a browser, or serve the folder:
```bash
python3 -m http.server 8000
```

## Updating data

Car specs, model-year variants, mods, remap platforms and garages are plain JavaScript arrays near the top of the `<script>` block in `index.html` (`CARS`, `VARIANTS`, `MODS`, `PLATFORM`, `GARAGES`).

## Disclaimer

A planning guide, not professional, legal or insurance advice. Power gains, costs and review scores are typical or point-in-time figures. Confirm with your insurer, a qualified technician and current GOV.UK guidance before modifying a car.
