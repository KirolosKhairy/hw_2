# Data Analysis Notebook (Polars & Pandas)

A practical notebook covering data analysis + performance optimization techniques using **Polars** and **Pandas**.

## What’s inside
### Part 1 — Polars: Titanic (train.csv)
- Read CSV with explicit `schema_overrides` (optimized dtypes)
- Basic profiling: shape, dtypes, null counts, describe
- Simple analysis:
  - Passenger count by class
  - Survivors by gender
  - Filter: `Age > 44`

### Part 2 — Pandas speedup: Titanic
- Fast statistics with **Bottleneck** (`nanmean`, `nanstd`)
- Vectorized feature engineering: `Fare_new` based on `Pclass`
- Quick sanity checks (`value_counts`, `isna`, `describe`)

### Part 3 — Pandas memory optimization: Housing.csv
- Suggest optimal dtypes (downcast ints/floats, boolean from text, low-cardinality → category, datetime attempt)
- Apply optimized dtypes and compare memory usage

## Key Result
- Memory reduced from **0.2167 MB** to **0.0124 MB** (≈ **94.30%** saving) on the Housing dataset.

## Tech Stack
- Python
- Jupyter Notebook
- Polars, PyArrow
- Pandas, NumPy
- Bottleneck

## How to Run
1. Put datasets in `data/`:
   - `data/train.csv`
   - `data/Housing.csv`
2. Open the notebook and run all cells.
