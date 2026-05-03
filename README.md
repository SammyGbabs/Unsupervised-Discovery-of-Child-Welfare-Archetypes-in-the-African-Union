# ISW 2026 Submission — Reproducibility Bundle

**Title:** *Multidimensional Child Welfare Profiles in Africa: A Pattern Recognition Approach to Country Archetypes Beyond Geographic Groupings*

## What's in this bundle

### Paper (LNCS submission)
- `main.tex` — paper source, ready to compile
- `main.pdf` — compiled paper (4 pages, real LNCS class)
- `fig_pca_compact.pdf` — single-panel PCA figure used in paper
- `fig_pca.pdf` — full two-panel PCA figure (kept for camera-ready / appendix)
- `fig_imputation.pdf` — imputation comparison bar chart (kept for camera-ready)
- `fig_contingency.pdf` — cluster–REC contingency heatmap (kept for camera-ready)
- LNCS class files: `llncs.cls`, `splncs04.bst`, `samplepaper.tex`, etc.

### Reproducibility
- `ISW2026_Child_Welfare_Archetypes.ipynb` — Colab-ready notebook that reproduces every experiment, table, and figure end-to-end
- `AfCSC-2026.xlsx` — input dataset (UNICEF Africa's Children 2026 Compendium)

### Generated data artifacts (from running the notebook)
- `clean_indicators.csv` — country × indicator matrix after cleaning
- `imputed_matrix.csv` — matrix after MF imputation
- `cluster_assignments.csv` — final cluster labels per country + REC + PCA coords
- `imputation_results.csv` — RMSE per imputation method
- `pca_loadings.csv` — top PCA component loadings

## Submission steps (today)

1. **Open the LNCS Overleaf template** from the ISW website.
2. **Replace `main.tex`** with the version in this bundle.
3. **Upload the figure PDFs** (`fig_pca_compact.pdf` is the one referenced in the 4-page version).
4. **Compile** — should produce 4 pages.
5. **Fill in your real name, affiliation, and email** at the top of `main.tex`.
6. **Submit** via https://chairingtool.com/conferences/isw2026/main-track before 03.05.2026.

## Reproducing the experiments (Colab)

1. Open `ISW2026_Child_Welfare_Archetypes.ipynb` in Google Colab.
2. Upload `AfCSC-2026.xlsx` to the Colab file panel.
3. Run all cells (≈2–3 minutes total). All paper numbers are reproduced; all figures are saved as PDFs.

## Key results reported in the paper

- **Imputation:** Matrix factorization achieves standardized RMSE of 0.918, a 16.6% reduction over column-mean baseline (1.101). Iterative MICE fails (RMSE 4.55) in the small-n/large-p regime.
- **Clustering:** Four stable archetypes recovered. Bootstrap within-cluster co-assignment 0.70 vs. between-cluster 0.13.
- **REC comparison:** ARI = 0.10 (k-means), NMI = 0.23 — data-driven welfare archetypes do not match Regional Economic Community structure.

## Citations to add for the camera-ready version

The 4-page submission cuts the bibliography to 5 essential refs to fit. For the 10-page camera-ready, restore:
- Troyanskaya et al. 2001 (k-NN imputation in Bioinformatics)
- Ward 1963 (hierarchical clustering)
- Strehl & Ghosh 2002 (NMI)
- A reference for SHAP if you add the supervised analysis
- Recent papers on cross-country child welfare clustering (search Google Scholar 2023–2025)