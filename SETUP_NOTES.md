# Hand-off / setup notes (delete this file before publishing)

This folder is a hand-off package mirroring the structure of
`R2RsquaredLSE/web-inflationdisasters`, with data and figures organized into
subfolders. Once the owner creates the GitHub repo and grants edit access,
do the following before the first push.

## Folder layout

```
.
├── README.md              # Top-level project page (rendered by GitHub Pages)
├── LICENSE                # MIT — fill in the copyright holder
├── _config.yml            # Jekyll config — fill in repo/owner placeholders
├── .gitignore
├── 25-infdis-bib.bib      # Bibliography entry for the paper
├── data/                  # Stata .dta files go here
│   └── README.md          # (lists expected filenames)
└── figures/               # PNG figures go here
    └── README.md          # (lists expected filenames)
```

## 1. Fill in placeholders

- **`LICENSE`** — replace `{{COPYRIGHT_HOLDER}}` with the chosen copyright
  holder (e.g. the GitHub org/user name, or the authors).
- **`_config.yml`** — replace:
  - `{{REPO_NAME}}` with the new repo name (used as the GitHub Pages baseurl).
  - `{{GITHUB_USERNAME}}` with the owner's GitHub username (twice — once in
    `url`, once in `github_username`).

## 2. Drop in the data and figures

**`data/`** (Stata):
- `USwestimates.dta`
- `EZwestimates.dta`

**`figures/`** (PNG):
- `figw_USinfshort.png`
- `figw_EZinfshort.png`
- `figw_USdefshort.png`
- `figw_EZdefshort.png`
- `figw_shorthorizon.png`
- `figw_USdensities.png`
- `figw_EZdensities.png`

**Paper (optional):**
- `25-infdis.pdf` at the repo root, if hosting the PDF alongside the data.

## 3. Enable GitHub Pages

After the first push:
1. Repo Settings → Pages → Source = `Deploy from a branch`, Branch = `main`, Folder = `/ (root)`.
2. Wait ~1 minute, then visit `https://{{GITHUB_USERNAME}}.github.io/{{REPO_NAME}}/`.

## 4. Delete this file (and the per-folder READMEs if desired)
`rm SETUP_NOTES.md` (or via the GitHub UI) once everything is in place.
The `data/README.md` and `figures/README.md` files can be kept as helpful
documentation or deleted once the real files are added.
