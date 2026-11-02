# Repository preparation

## Preserved source

The three completed notebooks, three starter notebooks, four CSVs, and one assignment PDF are copied unchanged. `SOURCE_MANIFEST.json` records their SHA-256 digests and uploaded-archive-relative origins. Original student/instructor attribution and saved outputs remain in the submission notebooks.

No separate report documents were included in the submission archives. Each `reports/results.md` is a newly written English explanation based on the assignment, code, and saved notebook outputs.

## Portable copies

The notebooks in `notebooks/` add a title and project-relative dataset lookup, clear execution counts and outputs, and retain the submitted analytical sequence. Minimal fixes are:

- Project 1: call `plt.boxplot(y)` without assigning its result to the imported `plt` module; use symmetric `numpy.linalg.eigh` for the covariance matrix so numerical roundoff does not produce complex-valued plot inputs.
- Project 2: use `reg:squarederror` instead of the deprecated `reg:linear` objective, label the square-root error as RMSE, and retain Boolean transaction features for Apriori.
- Project 3: dataset-path portability only; the original methodological choices and search grids are not rewritten.

The root requirements select a Python 3.11-compatible historical API environment. They are a compatibility specification, not a fully reproduced environment lock. Verify the installation before a complete rerun.
