# BS2023 — A Reassessment of Monetary Policy Surprises and High-Frequency Identification

**Paper.** Michael D. Bauer and Eric T. Swanson (2023), "A Reassessment of Monetary Policy Surprises and High-Frequency Identification", *NBER Macroeconomics Annual 2022*, vol. 37. [doi:10.1086/723574](https://doi.org/10.1086/723574) · [author's PDF](https://www.michaeldbauer.com/files/mps.pdf)

**Replication** by Isabella Bonetto, Irene Ferraioli, Lorenzo Giordani, Alessio Morrone and Tiziano Nocco.

## What it does

Uses the authors' published data (original 2022 release).

- Table 1, columns (1)–(3): high-frequency monetary policy surprises are predictable from data released before each FOMC announcement.
- The monthly instrument and its orthogonalized version, rebuilt from scratch and checked against the authors' series.
- Figure 3: a proxy SVAR identified with the raw or the orthogonalized surprise, with first-stage F statistics and wild-bootstrap bands.
- Figure 2: the same SVAR over the paper's three sample periods.

The results with Fed Chair speeches (Figure 4 onwards), Table 2 and column (4) of Table 1 cannot be replicated, because the data they need are not public.

## Main result

Table 1 matches the paper (coefficients exactly, t-statistics to within 0.01). With the orthogonalized instrument the fall in industrial production is about four times larger (−1.39% against −0.38%; the paper reports −1.4% and −0.35%), but the instrument becomes weak (first-stage F of about 2).

## Files

| Path | Content |
|---|---|
| `BS2023_replication.ipynb` | the notebook, with outputs |
| `data/monetary-policy-surprises-data.xlsx` | a reduced copy of the authors' data: the two `(original)` sheets with only the columns the notebook uses, values unchanged (the `Description` sheet describes each column and gives the source) |
| `figures/` | the figures saved by the notebook |
| `export_web.py` | runs the notebook's code and writes the data for the interactive panel on the website (to `../../data/replications/`, i.e. it expects this repository inside the website's folder) |

The full data, including the updates to 2023, are on the [San Francisco Fed's website](https://www.frbsf.org/research-and-insights/data-and-indicators/monetary-policy-surprises/).

## Running it

Open the notebook from this folder. It needs `numpy`, `pandas`, `matplotlib`, `statsmodels` and `openpyxl` (see `../requirements.txt`) and runs in about 25 seconds.
