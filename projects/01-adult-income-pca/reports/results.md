# Submitted analysis summary

## Objective and approach

Investigate the census table through data cleaning, descriptive plots, categorical encoding, and a direct mathematical implementation of PCA. The submitted notebook uses `StandardScaler`, constructs covariance matrices both explicitly and with `numpy.cov`, and orders eigenvectors by descending eigenvalue.

## Outputs present in the submission

- Plots examining age, hours worked, outliers, and pairwise relationships.
- Encoded and standardized data arrays.
- Covariance-matrix output and projections onto 10 and 2 principal components.
- Two-dimensional scatter and correlation heatmaps.

No predictive accuracy or explained-variance threshold is established by these outputs. The historical notebook is retained in `../submission/`; the figure in the project README is extracted from it.

## Limitations

The `income` column is included in categorical encoding; this is acceptable as a description of what was submitted but should not be interpreted as a target-excluded prediction pipeline. The covariance implementation uses general eigendecomposition rather than the symmetric-specialized alternative. The first heatmap correlates the two components with one another; the second combines encoded features and components, rather than selecting a feature/component-only block.

The portable copy corrects a box-plot statement that overwrote the `matplotlib.pyplot` module. It also uses symmetric `numpy.linalg.eigh` for the covariance matrix to avoid roundoff-related complex plotting inputs. The original general eigendecomposition remains unchanged in the archived submission.
