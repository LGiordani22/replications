# CEE2005 — Nominal Rigidities and the Dynamic Effects of a Shock to Monetary Policy

**Paper.** Lawrence J. Christiano, Martin Eichenbaum and Charles L. Evans (2005), "Nominal Rigidities and the Dynamic Effects of a Shock to Monetary Policy", *Journal of Political Economy* 113(1), 1–45. [doi:10.1086/426038](https://doi.org/10.1086/426038)

**Replication** by Isabella Bonetto, Irene Ferraioli, Lorenzo Giordani, Alessio Morrone and Tiziano Nocco.

## What it does

Section II of the paper: the VAR evidence on a monetary policy shock, 1965Q3–1995Q3. The DSGE model (Sections III–VI) is not replicated.

- A VAR(4) in nine U.S. aggregates, estimated by OLS and checked against `statsmodels`.
- Recursive identification with CEE's timing assumption, impulse responses with residual-bootstrap bands (2,000 replications), and the variance decomposition.
- A comparison with the paper's Figure 1 and Table 1.
- Robustness: commodity prices in the Fed's information set, and 2 or 6 lags instead of 4.

## Main result

Real activity has the paper's hump-shaped response: GDP peaks at about +0.5% after six quarters, consumption and investment follow the same pattern, and the variance shares lie inside CEE's 95% intervals except inflation at four quarters. The main difference is a price puzzle: prices fall for about a year and a half. Most of it disappears once commodity prices are added (the inflation dip goes from −0.26 to −0.12 points, as in the paper).

## Files

| Path | Content |
|---|---|
| `CEE2005_replication.ipynb` | the notebook, with outputs |
| `data/NominalRigidities.xlsx` | the FRED series the notebook uses, 1963Q4–1995Q3 (sheets `Quarterly` and `Monthly`; the `README` sheet lists each series, its units, vintage and use) |
| `figures/` | the figures saved by the notebook |
| `export_web.py` | runs the notebook's code and writes the data for the interactive panel on the website (to `../../data/replications/`, i.e. it expects this repository inside the website's folder) |

The data are today's FRED vintage (base year 2017), not the 2005 vintage CEE used, so the numbers cannot match the paper to the decimal.

## Running it

Open the notebook from this folder. It needs `numpy`, `pandas`, `matplotlib`, `statsmodels` and `openpyxl` (see `../requirements.txt`) and runs in about 15 seconds.
