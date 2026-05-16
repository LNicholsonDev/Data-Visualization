# Car Dealership Inventory Analysis

Two-notebook analysis of a 205-vehicle dealership inventory. The first 
notebook handles data cleaning, the second covers exploratory analysis, 
segmentation, and visualization of pricing trends by body type and 
engine characteristics.

---

## Key Findings

Turbocharged vehicles command consistently higher average prices than 
standard-aspiration vehicles across every body type in the dataset. 
Hardtop turbos have the highest average price at $28,176, while 
standard hatchbacks are the most affordable at $9,700.

Quantile segmentation divides the catalog into three price tiers:
low ($5,118–$8,449), medium ($8,495–$13,860), and high ($13,950–$45,400).

Scatterplots confirm positive relationships between price and both 
engine size and curb weight - larger, heavier vehicles skew toward 
the higher price tiers.

---

## Pipeline

**Notebook 1 — Data Cleaning**
- Splits brand names from model names via lambda expression to isolate 
  spelling errors in brand field
- Corrects 7 brand name errors (e.g. maxda→Mazda, porcshce→Porsche, 
  vw/vokswagen→Volkswagen, alfa-romero→Alfa Romeo)
- Renames columns for consistency and drops analytically irrelevant 
  fields (carid, symboling)

**Notebook 2 — Analysis**
- Melts enginesize and curbweight into a single feature column for 
  faceted scatterplot comparison against price
- Ranks rows by price and bins into low/medium/high tiers using 
  quantile-based pd.qcut()
- Groups by carbody and aspiration to compute mean price per segment, 
  then unstacks aspiration into columns for side-by-side comparison
- Replicates groupby result using pivot_table() to demonstrate 
  equivalent approaches
- Visualizes mean price by body type and aspiration as a grouped bar chart

---

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=flat&logo=python&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

---

[← Back to Data Visualization Projects](../)
