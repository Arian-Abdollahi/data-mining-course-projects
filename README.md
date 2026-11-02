# Data Mining Course Projects

Three Python/Jupyter coursework projects covering exploratory data analysis, dimensionality reduction, supervised learning, and association rule mining.

**Author:** Arian Abdollahi  
**Course:** Data Mining

## Projects

| Project | Focus | Main techniques | Explore |
| --- | --- | --- | --- |
| **01 · Adult Census Analysis and PCA** | Understand census features and project them into fewer dimensions | Missing-value filtering, one-hot encoding, standardization, PCA from scratch | [Project overview](projects/01-adult-income-pca/README.md) · [Notebook](projects/01-adult-income-pca/notebooks/adult_income_pca.ipynb) |
| **02 · Regression and Association Rules** | Predict real-estate prices and discover grocery purchase patterns | Linear/polynomial regression, Ridge, Lasso, Elastic Net, XGBoost, Apriori | [Project overview](projects/02-regression-and-association-rules/README.md) · [Notebook](projects/02-regression-and-association-rules/notebooks/regression_and_association_rules.ipynb) |
| **03 · Shopper Purchase Intention** | Investigate purchasing behavior and compare learning methods | PCA, SMOTE, SVM, KNN, logistic regression, decision trees, K-means, DBSCAN | [Project overview](projects/03-shopper-purchase-intention/README.md) · [Notebook](projects/03-shopper-purchase-intention/notebooks/purchase_intention.ipynb) |

## Quick start

Python **3.11** is recommended, matching the submitted notebooks' language metadata.

```bash
git clone https://github.com/Arian-Abdollahi/data-mining-course-projects.git
cd data-mining-course-projects
python -m venv .venv
```

Activate the environment:

```bash
# Linux / macOS
source .venv/bin/activate
# Windows PowerShell
# .venv\Scripts\Activate.ps1
```

Then install dependencies and launch Jupyter:

```bash
python -m pip install -r requirements.txt
python -m jupyterlab
```

Open a notebook from a project's `notebooks/` folder and run its cells in order. All four course-provided CSV files are included. Project 3's complete grid searches are computationally expensive; review its instructions before running every cell.

## Repository organization

Each project contains:

| Folder | Contents |
| --- | --- |
| `notebooks/` | Portable analysis notebook with outputs cleared before a fresh run |
| `submission/` | Original submitted notebook, unchanged, including historical saved outputs |
| `assignment/` | Original starter notebook; Project 2 also includes the supplied assignment PDF |
| `data/` | Course-provided CSV dataset(s) |
| `reports/` | English summary of the submitted analysis, results, and limitations |
| `figures/` | Representative figure extracted from the original notebook output |

The uploaded submissions contained notebooks rather than separate written reports. Their saved plots and outputs are preserved in `submission/`; the new English summaries explain those submissions. Only one assignment PDF was supplied, for Project 2. Projects 1 and 3 use their starter notebooks as the assignment briefs.

## Results and reproducibility

Saved outputs are **historical coursework results**, not newly reproduced benchmark claims. Project summaries distinguish training, cross-validation, and test-set measurements. In particular, Project 3 has evaluation limitations that should be considered when interpreting its scores.

See [verification and known limitations](docs/VERIFICATION.md), [repository preparation notes](docs/PREPARATION.md), and the [source checksum manifest](docs/SOURCE_MANIFEST.json).

## Skills demonstrated

- Data cleaning, visualization, categorical encoding, and scaling.
- Covariance matrices, eigendecomposition, and PCA implementation.
- Regression fitting, regularization, and error analysis.
- Transaction encoding, frequent itemsets, and association rules.
- Classification, class imbalance, hyperparameter search, and clustering.

## Attribution and data

The completed notebooks identify **Arian Abdollahi** as the student author. Original instructor/assignment attribution is retained in the source notebooks. The Project 2 template names Dr. Nazerfard as instructor and Farhad Aman as exercise designer; this is not attributed to the other projects without evidence.

Datasets and assignment materials are included as supplied for this coursework. Their original licensing/provenance was not provided in the archives. No license grant is added for the coursework, assignment text, or datasets. See [data notes](docs/DATA.md).

## Git workflow

For initial publication and subsequent changes, see [Git commands](docs/GIT_WORKFLOW.md).
