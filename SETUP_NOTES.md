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
└── figures/               # one PDF per series
    ├── US_5y_dens.pdf
    ├── US_10y_dens.pdf
    ├── EZ_5y_dens.pdf
    └── EZ_10y_dens.pdf
```

## Placeholders to fill when handing off to a different owner

- **`LICENSE`** — currently reads "Copyright (c) 2026 Nicholas Tokay" (trial). Replace with the final copyright holder.
- **`_config.yml`** — currently set to `nichtokay` / `Test_densities`. Replace `baseurl`, `url`, and `github_username` with the new owner's values.

## Updating the data later

Drop new csv/dta/xlsx files into `data/` (same names) and new PDFs into `figures/`. Then:

```
git add .
git commit -m "Update vintage"
git push
```

If at some point you want inline figure previews on the page (instead of PDF download links), regenerate PNGs from the PDFs with PyMuPDF and add them alongside, then point the README's image syntax at the PNGs.

## Enable GitHub Pages (first time only)

Repo Settings → Pages → Source = *Deploy from a branch*, Branch = `main`, Folder = `/ (root)` → Save. Visit `https://<owner>.github.io/<repo>/`.

## Delete this file
`git rm SETUP_NOTES.md && git commit -m "Remove hand-off notes" && git push` once everything is in place.
