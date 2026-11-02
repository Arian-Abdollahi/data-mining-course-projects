# Submitted results and evaluation context

## Data and experiment

The provided CSV contains 12,330 sessions: 10,422 non-purchase and 1,908 purchase sessions. The stratified split produces a 2,466-session test set (2,084 non-purchase and 382 purchase cases). The notebook uses six PCA components for classification and balances the training representation with SMOTE.

## Historical final test report

The final cell fits KNN with `n_neighbors=9`, Manhattan distance, and `algorithm='auto'` on the original, non-SMOTE PCA training data, then predicts the test set.

| Class | Precision | Recall | F1 | Support |
| --- | ---: | ---: | ---: | ---: |
| Non-purchase (-1) | 0.89 | 0.96 | 0.92 | 2,084 |
| Purchase (+1) | 0.62 | 0.37 | 0.46 | 382 |
| Macro average | 0.75 | 0.66 | 0.69 | 2,466 |

Saved test accuracy is **0.87**, rounded by the original classification report. This is a historical output, not a newly established performance guarantee. A majority-class baseline is about 84.5%, so accuracy alone conceals the low purchase-class recall.

## What the comparison figures mean

The model-comparison reports predict the SMOTE training data that the models were fitted on. They therefore show training/resubstitution performance, not held-out generalization. The decision tree's perfect saved training score is not a perfect test result.

The saved KNN grid winner uses three neighbors and Euclidean distance, while the separately configured final KNN uses nine neighbors and Manhattan distance. These are different experiments, and the final model is not the saved grid-search winner.

## Limitations to address in future work

1. Box-Cox parameters and categorical encodings are fitted before the train/test split. Fit learned preprocessing inside training folds for a clean predictive evaluation.
2. Training scaling/PCA and SMOTE are performed before the grid-search cross-validation folds. Use an imbalanced-learn pipeline so each fold fits transformations and resampling only on its own training partition.
3. The logistic-regression grid contains incompatible solver/penalty combinations; failed candidates can produce warnings. It has no `saga` option for its elastic-net candidates.
4. The final KNN is fitted without SMOTE, unlike the earlier model comparisons. Clearly distinguish these variants.
5. Exploratory full-data PCA is separate from predictive training PCA. Only the latter is fitted after the split, and it is still outside the CV folds.
6. Classification reports on arbitrary cluster IDs do not establish clustering quality. Appropriate clustering metrics or an explicitly justified label alignment are needed.
7. K-means initialization and decision-tree randomness are not fully fixed in the original submission. Saved outputs may differ on rerun.
8. The assignment requests ROC-AUC comparisons, but the submitted comparison charts show precision, recall, and F1 rather than a complete requested metric panel.

The repository preserves these coursework decisions and documents them. It does not silently replace the original experiment with a new pipeline.
