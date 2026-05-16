# Forest Fires by State 1992–2015

Data preparation and aggregation pipeline applied to U.S. wildfire 
records across all 50 states over 23 years. The two notebooks in this 
project cover the full wrangling workflow: raw data preparation in 
the first, and grouping, pivoting, and decade-level aggregation in 
the second.

---

## What the Data Shows

The decade-level aggregation surfaces patterns not visible in annual 
snapshots. Alaska's 2000s decade represents the highest burn volume 
of any state in any period in the dataset - 18.9 million acres across 
974 fires. The 2010s partial decade (2010–2015) already shows 8.4 
million acres for Alaska alone, with 2015 accounting for 5.1 million 
of those acres across 340 fires and 16,636 days burning.

Fire count and acreage do not reliably correlate. California recorded 
819 fires in 1992 with 289K acres burned; Alaska recorded 144 fires 
in 1993 with 687K acres - a pattern that holds across the dataset and 
illustrates why fire count alone is a poor proxy for fire severity.

Fire activity is strongly seasonal. Alaska peak burn months are June 
and July, with June 1997 recording approximately 1.6 million acres - 
the most striking single-month outlier visible in the prepared data.

---

## Pipeline

**Notebook 1 — Prepare Data**
- Derives `mean_acres_burned_daily` (acres_burned ÷ days_burning) with 
  explicit division-by-zero handling via lambda expression
- Converts fire_month from integer to abbreviated string (5 → 'May')
- Constructs a three-level multi-index on state, fire_year, fire_month
- Unstacks fire_month to wide format for cross-month comparison
- Demonstrates safe copy semantics to avoid SettingWithCopyWarning
- Appends new records and resets index with drop=True

**Notebook 2 — Process Data**
- Groups by state and fire_year, summing acres_burned, days_burning, 
  and fire_count into annual totals
- Pivots recent years (2013–2015) into a state × year acreage matrix 
  using both pivot() and pivot_table() for comparison
- Bins fire_year into decades using pd.cut() with custom edges
- Produces a state × decade summary table of total burn metrics

---

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

---

[← Back to Data Visualization Projects](../)
