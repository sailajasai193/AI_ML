Data Cleaning – Handling Missing Values

**Dataset used:** `winequality-red_miss.csv` (with missing values) and `winequality-red_original.csv` (original reference file).

---
## What was done:

### Missing Values Analysis
- Displayed the number of missing values in each attribute and total missing values.
- Deleted and replaced certain integer values in **fixed acidity** and **volatile acidity** with `NaN` / `N/A` to simulate missing data.
- Ensured detection of `"na"` as missing values (`pd.NA`).
- Saved modified versions (`winequality-red_miss-modified.csv`, `winequality-red_cleaned.csv`, `winequality-red_target_cleaned.csv`).

### Cleaning Steps
- Counted tuples with 1–12 missing values and plotted **Missing Values vs Tuples**.
- Counted tuples with **≥50% missing attributes** and dropped them.
- Dropped tuples with missing **quality** (target attribute).
- Saved cleaned datasets.

### Experiments on Filling Missing Values
- Replaced missing values using:
  - **Median filling** (`fillna()` with median values).
  - **Forward fill** (propagating previous non-missing values).
  - **Linear interpolation** (`interpolate()`).
- Computed **Mean, Median, Mode, Std** for each attribute and compared with the original dataset.
- Calculated **RMSE** (Root Mean Square Error) and **RMSE%** to evaluate closeness of filled values to original data.

---
