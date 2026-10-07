# Replications

Replications of published papers in macroeconomics and macro-finance, in Python. Each folder has a notebook with its outputs, the data it uses, the figures it saves, and its own README with the full reference to the paper and the authors of the replication.

| Folder | Paper | Replication by |
|---|---|---|
| [`CEE2005`](CEE2005) | Christiano, Eichenbaum and Evans (2005), "Nominal Rigidities and the Dynamic Effects of a Shock to Monetary Policy", *Journal of Political Economy* | I. Bonetto, I. Ferraioli, L. Giordani, A. Morrone, T. Nocco |
| [`BS2023`](BS2023) | Bauer and Swanson (2023), "A Reassessment of Monetary Policy Surprises and High-Frequency Identification", *NBER Macroeconomics Annual* | I. Bonetto, I. Ferraioli, L. Giordani, A. Morrone, T. Nocco |
| [`ABG2019`](ABG2019) | Adrian, Boyarchenko and Giannone (2019), "Vulnerable Growth", *American Economic Review* | L. Giordani |

## Running the notebooks

```
pip install -r requirements.txt
```

Then open a notebook from its own folder (paths to `data/` and `figures/` are relative). Every notebook runs top to bottom with fixed seeds and reproduces the stored outputs.

The papers themselves are not included; each README links to them.

## License

The code and notebooks are released under the [MIT License](LICENSE). The data files are not covered by it: they come from FRED and from the papers' authors, and remain subject to their sources' terms (each data file names its source).
