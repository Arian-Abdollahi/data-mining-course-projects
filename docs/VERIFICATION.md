# Verification and execution coverage

## Source and structure checks

- All 11 archived source files match their recorded SHA-256 digests.
- All code cells in the three portable notebooks parse as Python.
- The portable notebooks contain no Windows-specific dataset paths or stale outputs.
- All four CSVs have the documented record counts, column counts, and consistent row widths.
- Project 3's assignment and submission CSVs are byte-identical.

## Execution performed during preparation

| Project | Executed successfully | Not executed |
| --- | --- | --- |
| 1 | Complete portable notebook, including cleaning, plots, encoding, standardization, PCA, and heatmaps; 45,222 rows remain after filtering | Nothing in the portable analysis sequence |
| 2 | Data loading, feature selection, split, exploratory plots, linear/polynomial/Ridge/Lasso/Elastic Net regression | XGBoost and Apriori; their packages were unavailable in the checking environment |
| 3 | Data loading, transformations, stratified split, regression baseline, exploratory/training PCA, classifier imports, final KNN test, and confusion matrix | SMOTE, full hyperparameter grids, training-comparison plots, K-means, and DBSCAN |

The Project 3 KNN check produced **0.8665855636658556 accuracy** on the supplied 2,466-session test set. It is a partial reproduction of the final-model section, not a validation of the original search procedure or removal of its preprocessing limitations.

The checking environment used Python 3.12, NumPy 2.3.5, Pandas 2.2.3, SciPy 1.17.0, scikit-learn 1.8.0, Matplotlib 3.10.8, and Seaborn 0.13.2. This differs from the Python 3.11 compatibility environment specified in `requirements.txt`; a full clean installation of that environment has not been verified. In particular, the unchanged original logistic-regression grid requires the older API retained by the requirements.

## Known limitations

Read each project's report for methodological details. Project 3's preprocessing, resampling outside CV, training-set comparisons, final-model selection differences, and arbitrary clustering-label comparisons limit interpretation of its saved results. Project 2 does not print Elastic Net error metrics. Historical outputs are preserved as source evidence rather than certified benchmark claims.
