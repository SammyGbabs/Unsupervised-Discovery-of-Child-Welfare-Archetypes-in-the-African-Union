# ISW 2026 Submission — Reproducibility Bundle

**Title:** *Unsupervised Discovery of Child Welfare Archetypes Across the African Union.*

## What's in this bundle

### Paper (LNCS submission)
- `paper/main.tex` — paper source, ready to compile
- `paper/main.pdf` — compiled paper (4 pages, real LNCS class)
- `figures/fig_pca_compact.pdf` — single-panel PCA figure used in paper
- `figures/fig_pca.pdf` — full two-panel PCA figure (kept for camera-ready / appendix)
- `figures/fig_imputation.pdf` — imputation comparison bar chart (kept for camera-ready)
- `figures/fig_contingency.pdf` — cluster–REC contingency heatmap (kept for camera-ready)
- LNCS class files: `llncs.cls`, `splncs04.bst`, `samplepaper.tex`, etc.

### Reproducibility
- `ISW2026_Child_Welfare_Archetypes.ipynb` — Colab-ready notebook that reproduces every experiment, table, and figure end-to-end
- `data/AfCSC-2026.xlsx` — input dataset (UNICEF Africa's Children 2026 Compendium)

### Generated data artifacts (from running the notebook)
- `artifacts/clean_indicators.csv` — country × indicator matrix after cleaning
- `artifacts/imputed_matrix.csv` — matrix after MF imputation
- `artifacts/cluster_assignments.csv` — final cluster labels per country + REC + PCA coords
- `artifacts/imputation_results.csv` — RMSE per imputation method
- `artifacts/pca_loadings.csv` — top PCA component loadings

## Reproducing the experiments (Colab)

1. Open `ISW2026_Child_Welfare_Archetypes.ipynb` in Google Colab.
2. Upload `data/AfCSC-2026.xlsx` to the Colab file panel.
3. Run all cells (≈2–3 minutes total). All paper numbers are reproduced; all figures are saved as PDFs.

## Key results reported in the paper

- **Imputation:** Matrix factorization achieves standardized RMSE of 0.913, a 17% reduction over column-mean baseline (1.101). Iterative MICE fails (RMSE 4.55) in the small-n/large-p regime.
- **Clustering:** Four stable archetypes recovered. Bootstrap within-cluster co-assignment 0.70 vs. between-cluster 0.13.
- **REC comparison:** ARI = 0.10 (k-means), NMI = 0.23 — data-driven welfare archetypes do not match Regional Economic Community structure.

## Citations to add for the camera-ready version

The 4-page submission cuts the bibliography to 5 essential refs to fit. For the 10-page camera-ready, restore:
- Troyanskaya et al. 2001 (k-NN imputation in Bioinformatics)
- Ward 1963 (hierarchical clustering)
- Strehl & Ghosh 2002 (NMI)
- A reference for SHAP if you add the supervised analysis
- Recent papers on cross-country child welfare clustering (search Google Scholar 2023–2025)