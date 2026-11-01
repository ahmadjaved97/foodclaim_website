# FoodClaim website

A lightweight, responsive project page for **FoodClaim: A Benchmark for Detecting Generated and Manipulated Food Defects**, accepted at WACV 2027. Plain HTML, CSS, and JavaScript; no dependencies or build step.

## Preview locally

From this directory, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open <http://127.0.0.1:8000>. Stop the server with Ctrl+C.

## Update content

- `index.html`: authors, text, statistics, resource availability, and preliminary BibTeX.
- `styles.css`: colors are CSS variables at the top; change `--accent` and `--accent-dark` to adjust the green theme.
- `assets/`: main-paper and supplementary figures, optimized as WebP, and the favicon. Each figure links to its larger image.
- `script.js`: optional copy-to-clipboard behavior. The full page works without JavaScript.

The code resource links to https://github.com/ahmadjaved97/FoodClaim. The paper and Hugging Face dataset are marked **Coming soon**; replace their `.resource` divs with anchors when the public URLs are ready. The preliminary citation should be updated with final publication details.

The introduction reproduces the paper’s abstract. The construction section uses Figure 3 and a shortened source caption, with Figure 2 in an expandable section. Category totals aggregate Table S14, and an expandable table preserves its full counts. The Image Generators section presents Table S15; the Baselines section reproduces Table 5 in an overall/ID/OOD table and an expandable per-class F1 table. The page includes Figures 1–3 and matched examples S3–S8, with additional examples in expandable sections. The plausibility study and its charts are omitted. Figure and table numbers are omitted on the page. Tables and galleries work without JavaScript.

Source consistency note: the supplied abstract reports 88.2%/63.8% seen/held-out accuracy; the supplied Table 5 reports different baseline values. The website preserves the abstract and Table 5 independently, without replacing either set of numbers. Reconcile them when the manuscript is finalized.

The source manuscript and review PDF are excluded from Git. Add the public paper version when ready. The page leaves dataset licensing unspecified until release details are available.

## Publish later on GitHub Pages

Git was initialized locally on `main` before website implementation. No GitHub remote or hosted deployment has been created.

Create an empty repository in your GitHub account, then connect and push this folder. Commit the website files first if you have not already done so:

```sh
git add .gitignore README.md index.html styles.css script.js assets .nojekyll
git commit -m "Create FoodClaim dataset website"
git remote add origin https://github.com/YOUR_ACCOUNT/YOUR_REPOSITORY.git
git push -u origin main
```

In the GitHub repository settings, enable Pages using **Deploy from a branch**, branch **main**, folder **/ (root)**. All local website asset paths are relative so they also work under a repository subpath.
