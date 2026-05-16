# Child Mortality Trends 1900–2018

Two-notebook analysis of U.S. child mortality across four pediatric age 
groups (ages 1–4, 5–9, 10–14, and 15–19) spanning 119 years from 
1900 to 2018. The first notebook covers data preparation and exploratory 
analysis; the second contains the full visualization suite.

---

## Key Findings

Total childhood mortality across all four age groups fell from 3,233 
deaths per 100k in 1900 to 99.6 per 100k in 2018 (a decline of over 
96%). The 1–4 age group had the highest absolute death rate throughout 
the dataset (1,983.8 per 100k in 1900), declining to 24.0 per 100k 
by 2018.

The most pronounced anomaly in the data is 1918. The 15–19 age group 
spiked from 380.3 per 100k in 1917 to 777.4 in 1918 before returning 
to 438.5 in 1919. All four age groups spike sharply in 1918, consistent 
with the influenza pandemic, before resuming the long-term downward trend.

---

## Notebooks

**Notebook 1 — Prepare & Explore**
- Reads long and wide format mortality data
- Renames `DeathRate` to `Deaths/100k` for clarity
- Queries subsets by year range and age group
- Sorts by death rate to identify highest and lowest recorded values
- Groups by year with mean, median, and sum aggregations
- Derives `TotalDeaths` summing across all four age groups
- Line plot of total death rate by year

**Notebook 2 — Full Visualization Suite**
- Annotated line plots by age group with confidence intervals
- Bar charts and categorical plots for cross-group comparison
- Histograms, ECDF, and KDE plots for distributional analysis
- Box plots for spread and outlier identification
- Line plots isolating selected year ranges for period-specific examination
- Subplots for multi-panel comparison across age groups

---

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=flat&logo=python&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

---

[← Back to Data Visualization Projects](../)
