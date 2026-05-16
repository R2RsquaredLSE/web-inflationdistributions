.
# Summary
The prices of inflation options give the cost of insuring against extreme events. They reveal the **full probability distribution of future inflation** as perceived by market participants. To construct these distributions at horizons beyond the immediate, the standard option pricing formulas have to be modified in three ways: to account for the erosion of the real value of the options' payoff, to account for the forward starting horizon, and to account for the compensation for inflation risk. Below are estimated probability densities of average future inflation, making these adjustments. The data starts in October 2009 (US) / January 2010 (Euro Area) and covers monthly snapshots through February 2026. This dataset can be **freely used** by other researchers.

The dataset will be updated regularly to reflect the latest data.
- **Vintage 1:** The dataset was first released in May 2026 to cover densities until February 2026.

---

# Authors and Reference:
[How Likely Is an Inflation Disaster?](https://doi.org/10.1093/rfs/hhaf058) (2025), Review of Financial Studies,  hhaf058, October. 
[bibtex](25-infdis-bib.bib)
- [Jens Hilscher](https://hilscher.ucdavis.edu)
- [Alon Raviv](https://mba.biu.ac.il/en/raviv)
- [Ricardo Reis](https://www.r2rsquared.com/)
- Acknowledgments: Daniel Albuquerque, Marina Feliciano, Seyed Mahdi Hosseini, Rui Sousa, Nicholas Tokay, and Borui Zhu provided excellent research assistance.

---

# Probability densities
For each region and horizon, the dataset gives the full estimated density of average annualized inflation over the horizon, sampled at **21 support points** (every 0.5 percentage point from −3% to +7%), at monthly snapshot dates.

Each series is available in four formats — Stata, Excel, comma-separated, and a PDF figure of the latest snapshot.

| Region & horizon | Stata | Excel | CSV | PDF figure |
|---|---|---|---|---|
| United States, 5-year  | [.dta](data/US_5y_dens.dta)  | [.xlsx](data/US_5y_dens.xlsx)  | [.csv](data/US_5y_dens.csv)  | [.pdf](figures/US_5y_dens.pdf)  |
| United States, 10-year | [.dta](data/US_10y_dens.dta) | [.xlsx](data/US_10y_dens.xlsx) | [.csv](data/US_10y_dens.csv) | [.pdf](figures/US_10y_dens.pdf) |
| Euro Area, 5-year      | [.dta](data/EZ_5y_dens.dta)  | [.xlsx](data/EZ_5y_dens.xlsx)  | [.csv](data/EZ_5y_dens.csv)  | [.pdf](figures/EZ_5y_dens.pdf)  |
| Euro Area, 10-year     | [.dta](data/EZ_10y_dens.dta) | [.xlsx](data/EZ_10y_dens.xlsx) | [.csv](data/EZ_10y_dens.csv) | [.pdf](figures/EZ_10y_dens.pdf) |

---

# Variables
Each file is a long-format time series with three columns.

<table>
  <tr style="background-color: #d4f4d3;">
    <th style="border: 2px solid #68b684; padding: 8px;">Column</th>
    <th style="border: 2px solid #68b684; padding: 8px;">Description</th>
  </tr>
  <tr style="background-color: #f5f5f5;">
    <td style="border: 2px solid #68b684; padding: 8px;"><code>date</code></td>
    <td style="border: 2px solid #68b684; padding: 8px;">Snapshot date (YYYY-MM-DD)</td>
  </tr>
  <tr style="background-color: #d4f4d3;">
    <td style="border: 2px solid #68b684; padding: 8px;"><code>support</code></td>
    <td style="border: 2px solid #68b684; padding: 8px;">Inflation support point (annualized, decimal). Range: −0.03 to 0.07 in 0.005 steps (21 values)</td>
  </tr>
  <tr style="background-color: #f5f5f5;">
    <td style="border: 2px solid #68b684; padding: 8px;"><code>frequency</code></td>
    <td style="border: 2px solid #68b684; padding: 8px;">Estimated density at <code>(date, support)</code></td>
  </tr>
</table>

---

# Latest Figures

Each figure overlays selected snapshot dates (e.g. Mar 2020 through Mar 2024) so the post-COVID shift in inflation expectations is visible. Click to download the PDF.

## United States, 5-year horizon
📄 [Download figure (PDF)](figures/US_5y_dens.pdf)

Probability densities for US inflation averaged over the next 5 years, shown at selected snapshot dates.

---

## United States, 10-year horizon
📄 [Download figure (PDF)](figures/US_10y_dens.pdf)

Probability densities for US inflation averaged over the next 10 years, shown at selected snapshot dates.

---

## Euro Area, 5-year horizon
📄 [Download figure (PDF)](figures/EZ_5y_dens.pdf)

Probability densities for Euro Area inflation averaged over the next 5 years, shown at selected snapshot dates.

---

## Euro Area, 10-year horizon
📄 [Download figure (PDF)](figures/EZ_10y_dens.pdf)

Probability densities for Euro Area inflation averaged over the next 10 years, shown at selected snapshot dates.

---

# Usage
Please cite if used, and e-mail the authors with suggested corrections.
