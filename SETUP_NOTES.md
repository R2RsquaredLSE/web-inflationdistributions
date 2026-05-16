# Hand-off / setup notes (delete this file before publishing)

This folder mirrors the structure of `R2RsquaredLSE/web-inflationdisasters`, adapted to publish **probability densities of future inflation** rather than disaster probabilities. Once the final owner creates the GitHub repo and grants edit access, the only remaining steps are:

## Folder layout

```
.
├── README.md              # Top-level page (rendered by GitHub Pages)
├── LICENSE                # MIT
├── _config.yml            # Jekyll config (title, baseurl, theme)
├── .gitignore
├── 25-infdis-bib.bib      # Bibliography entry for the paper
├── data/                  # csv / dta / xlsx, one of each per series
│   ├── README.md
│   ├── US_5y_dens.{csv,dta,xlsx}
│   ├── US_10y_dens.{csv,dta,xlsx}
│   ├── EZ_5y_dens.{csv,dta,xlsx}
│   └── EZ_10y_dens.{csv,dta,xlsx}
└── figures/               # PDF + PNG preview per series
    ├── US_5y_dens.{pdf,png}
    ├── US_10y_dens.{pdf,png}
    ├── EZ_5y_dens.{pdf,png}
    └── EZ_10y_dens.{pdf,png}
```

## Placeholders to fill when handing off to a different owner

- **`LICENSE`** — currently reads "Copyright (c) 2026 Nicholas Tokay" (trial). Replace with the final copyright holder.
- **`_config.yml`** — currently set to `nichtokay` / `Test_densities`. Replace `baseurl`, `url`, and `github_username` with the new owner's values.

## Updating the data later

Drop new csv/dta/xlsx files into `data/` (same names) and new PDFs into `figures/`. To refresh the inline PNG previews:

```
cd figures
python -c "import fitz
for n in ['US_5y','US_10y','EZ_5y','EZ_10y']:
    d=fitz.open(f'{n}_dens.pdf'); d[0].get_pixmap(matrix=fitz.Matrix(2,2)).save(f'{n}_dens.png'); d.close()"
```

Then `git add . && git commit -m "Update vintage" && git push`.

## Enable GitHub Pages (first time only)

Repo Settings → Pages → Source = *Deploy from a branch*, Branch = `main`, Folder = `/ (root)` → Save. Visit `https://<owner>.github.io/<repo>/`.

## Delete this file
`git rm SETUP_NOTES.md && git commit -m "Remove hand-off notes" && git push` once everything is in place.
