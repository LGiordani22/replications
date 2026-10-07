# ABG2019 — Vulnerable Growth

**Paper.** Tobias Adrian, Nina Boyarchenko and Domenico Giannone (2019), "Vulnerable Growth", *American Economic Review* 109(4), 1263–1289. [doi:10.1257/aer.20161923](https://doi.org/10.1257/aer.20161923) · working-paper version: [New York Fed Staff Report 794](https://www.newyorkfed.org/research/staff_reports/sr794.html), which has the same figures and is the version the notebook's equation numbers refer to.

**Replication** by Lorenzo Giordani.

## What it does

Everything is computed from one data file: real GDP growth and the NFCI, 1973Q1–2015Q4.

- Quantile regressions of future GDP growth on current growth and financial conditions (Figures 2–6), with bootstrap bands under a linear Gaussian null.
- A skewed t-distribution fitted every quarter to the predicted quantiles, giving the full predictive density (Figures 1, 7–8, A.1–A.4).
- Downside and upside entropy, expected shortfall and longrise (Figure 9).
- A recursive out-of-sample exercise from 1993 (Figures 10–11) and the paper's two alternative approaches (Figures 12, A.8).
- Mean, volatility and entropy (Figures 13–14), plus a few additions of ours: fitting errors, a kernel estimate of the unconditional density, and a simple vulnerability measure.

## Main result

Financial conditions move the left tail of future growth much more than the centre or the right tail. Downside risk spikes in 1974–75, 1980–82 and 2008–09, and it would have been visible in real time. The predicted quantiles and the skewed-t parameters coincide with those of the authors' replication files.

## Files

| Path | Content |
|---|---|
| `ABG2019_replication.ipynb` | the notebook, with outputs |
| `data/DataVulnerability.xlsx` | the authors' data (FRED), 1973Q1–2015Q4, sheet `Data`; the `Legend` sheet describes the two series |
| `figures/` | the figures saved by the notebook, including the interactive `gdp_distribution_3d.html` |
| `export_web.py` | runs the notebook's code and writes the data for the interactive panel on the website (to `../../data/replications/`, i.e. it expects this repository inside the website's folder) |

## Running it

Open the notebook from this folder. It needs `numpy`, `pandas`, `scipy`, `matplotlib`, `plotly` and `openpyxl` (see `../requirements.txt`) and runs in about 5 minutes, mostly for the bootstrap.
