# Data

Estimated probability densities of average future annualized inflation, by region and horizon. Each series is provided in three machine-readable formats; the PDF version of the corresponding figure lives in `../figures/`.

| Series | Stata | Excel | CSV |
|---|---|---|---|
| US, 5-year   | `US_5y_dens.dta`  | `US_5y_dens.xlsx`  | `US_5y_dens.csv`  |
| US, 10-year  | `US_10y_dens.dta` | `US_10y_dens.xlsx` | `US_10y_dens.csv` |
| EA, 5-year   | `EZ_5y_dens.dta`  | `EZ_5y_dens.xlsx`  | `EZ_5y_dens.csv`  |
| EA, 10-year  | `EZ_10y_dens.dta` | `EZ_10y_dens.xlsx` | `EZ_10y_dens.csv` |

**Columns** (same in every file):
- `date` — snapshot date (YYYY-MM-DD)
- `support` — inflation support point (annualized, decimal), 21 values from −0.03 to 0.07 in 0.005 steps
- `frequency` — estimated density at that (date, support)

**Coverage:** US from 2009-10-05, EA from 2010-01-13, both running through 2026-02 — monthly snapshots, ≈ 197 dates × 21 support points per series.
