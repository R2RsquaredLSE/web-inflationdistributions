# Figures

One PDF per series (the high-resolution version, for downloads / inclusion in papers) plus a PNG preview at the same resolution (for inline display on the GitHub Pages site).

| Series | PDF | PNG preview |
|---|---|---|
| US, 5-year   | `US_5y_dens.pdf`  | `US_5y_dens.png`  |
| US, 10-year  | `US_10y_dens.pdf` | `US_10y_dens.png` |
| EA, 5-year   | `EZ_5y_dens.pdf`  | `EZ_5y_dens.png`  |
| EA, 10-year  | `EZ_10y_dens.pdf` | `EZ_10y_dens.png` |

Each figure overlays selected snapshot dates (e.g. Mar 2020, Mar 2021, …, Mar 2024) so the post-COVID shift in inflation expectations is visible.

**Regenerating PNGs from PDFs** (in case the source PDFs are updated):
```
python -c "import fitz
for n in ['US_5y','US_10y','EZ_5y','EZ_10y']:
    d=fitz.open(f'{n}_dens.pdf'); d[0].get_pixmap(matrix=fitz.Matrix(2,2)).save(f'{n}_dens.png'); d.close()"
```
