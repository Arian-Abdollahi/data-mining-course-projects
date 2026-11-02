# Submitted results and interpretation

These figures are transcribed from the original saved notebook outputs. They have not all been independently reproduced during repository preparation.

## Regression results

| Model | Test MAE | Test RMSE |
| --- | ---: | ---: |
| Linear regression | 6.5163 | 10.7157 |
| Polynomial regression (degree 2) | 5.7501 | 10.0778 |
| Ridge (`alpha=1`) | 6.5161 | 10.7156 |
| Lasso (`alpha=10`) | 7.0009 | 11.0496 |
| Elastic Net (`alpha=10`) | Not printed | Not printed |
| XGBoost (`gblinear`, 10 boosting rounds) | Not printed | 10.8819 |

Polynomial regression has the lowest saved RMSE among the models with printed RMSE values; this is a single-split comparison, not a cross-validated superiority claim. The original linear-regression output calls RMSE `mse` despite taking a square root. The portable notebook corrects this label.

The saved Lasso coefficients set the convenience-store coefficient to zero. Because features were not standardized before fitting the regularized models, coefficient penalties act on differently scaled inputs. No exhaustive tuning or statistical significance analysis was performed.

## Association rules

After transaction-string deduplication, the saved results report four rules:

| Antecedent | Consequent | Support | Confidence | Lift |
| --- | --- | ---: | ---: | ---: |
| BISCUIT | BREAD | 0.2353 | 0.6667 | 1.0303 |
| MILK | BREAD | 0.2353 | 0.8000 | 1.2364 |
| MAGGI | TEA | 0.2353 | 0.8000 | 2.2667 |
| TEA | MAGGI | 0.2353 | 0.6667 | 2.2667 |

These describe co-occurrence in a very small dataset, not causal effects or guaranteed sales gains. Transaction deduplication changes the empirical shopping distribution. Product labels such as `COCK` and `SUGER` are preserved exactly as supplied.

## Assignment coverage

The PDF asks for six regression methods, comparison of results, transaction cleaning, frequent itemsets, and association rules. The submission implements all six regressors, but Elastic Net error metrics are not printed. This English summary explains the saved notebook; no separate student report was present in the archive.
