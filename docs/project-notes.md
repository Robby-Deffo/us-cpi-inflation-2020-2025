# Project Notes — U.S. CPI Inflation Analysis

## Purpose

This project investigates U.S. consumer price trends from **January 2020 onward** using BLS CPI-U (Not Seasonally Adjusted) data. It focuses on three non-discretionary spending categories — **Food**, **Gasoline**, and **Shelter** — and includes a regional comparison with the **Los Angeles–Long Beach–Anaheim metro area** (California).

The goal is to produce clean, reproducible analysis and visualizations that communicate both the magnitude and persistence of post-pandemic inflation across key household cost categories.

---

## Tools & Environment

| Tool | Purpose |
|---|---|
| Python 3.x | Primary analysis language |
| Pandas | Data cleaning, wrangling, and computation |
| Matplotlib | Line chart visualizations |
| Seaborn | Correlation heatmap |
| Jupyter Notebook | Interactive development environment |
| VS Code | IDE |

---

## Data Source

**U.S. Bureau of Labor Statistics (BLS)**  
CPI-U — All Urban Consumers, Not Seasonally Adjusted  
Retrieved via BLS Data Finder: [https://www.bls.gov/cpi/](https://www.bls.gov/cpi/)

| BLS Series ID | File Name | Description |
|---|---|---|
| `CUUR0000SAF` | `CPI_U.S-Food.csv` | Food & Beverages, U.S. City Average |
| `CUUR0000SETB01` | `CPI_U.S-Gas.csv` | Gasoline (All Types), U.S. City Average |
| `CUUR0000SAH1` | `CPI_U.S-Shltr.csv` | Shelter, U.S. City Average |
| `CUURS49ASA0` | `CPI_CA-LA.csv` | All Items, Los Angeles–Long Beach–Anaheim, CA |

---

## What CPI Measures

The Consumer Price Index (CPI) measures the average change over time in prices paid by urban consumers for a representative basket of goods and services. It does not reflect actual dollar prices — it reflects a price *index* relative to a reference base period (typically 1982–1984 = 100).

**Example interpretation:**

| Date | Food CPI |
|---|---|
| Jan 2020 | 260.0 |
| Dec 2024 | 312.0 |

A CPI of 312 means prices are approximately 3.12× higher than in the 1982–1984 base period. For this project, we re-index to **January 2020 = 0%** to isolate post-pandemic inflation.

---

## Methodology

**Step 1 — Data Retrieval & Cleaning**
- Download CSVs from BLS, parse date columns, check for missing values
- Align all series to a common monthly date range (Jan 2020 – present)

**Step 2 — Baseline Indexing**
Compute percent change from the January 2020 baseline for each series:

$$\text{PctChange}_t = \frac{\text{CPI}_t - \text{CPI}_{\text{Jan 2020}}}{\text{CPI}_{\text{Jan 2020}}} \times 100$$

**Step 3 — Statistical Summary**
- Compute mean, median, 75th percentile, max, and standard deviation for each category

**Step 4 — Visualization**
- Individual line charts per category (Food, Gas, Shelter, California)
- Combined overlay chart for direct comparison
- Pearson correlation heatmap across all four series

**Step 5 — Output**
- Cleaned dataset saved to `data/processed/CPI_Percent_Change_Final.csv`
- Charts saved to `figures/`

---

## Output Files

| File | Description |
|---|---|
| `data/processed/CPI_Percent_Change_Final.csv` | Tidy dataset with % change columns for all four series |
| `figures/food_cpi_chart.png` | Food CPI line chart |
| `figures/gas_cpi_chart.png` | Gasoline CPI line chart |
| `figures/shelter_cpi_chart.png` | Shelter CPI line chart |
| `figures/cali_cpi_chart.png` | California metro CPI line chart |
| `figures/combined_cpi_comparison_chart.png` | All four series overlaid |
| `figures/cpi_correlation_heatmap.png` | Pearson correlation matrix |

---

*Author: Robby Deffo | CSUN M.S. Business Analytics (May 2026)*
