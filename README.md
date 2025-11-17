# CPI Inflation Analysis (U.S., 2020 – Present)

This repository contains **Part 1** of my CPI inflation project: a reproducible analysis of U.S. consumer price trends since January 2020. It focuses on **Food**, **Gasoline**, and **Shelter**, with a California (LA) metro comparison.

> Part 2 (in progress): U.S. geospatial CPI map by region/metro, and predictive modeling.

---

## Repository Structure

| Path | Description |
|---|---|
| `notebooks/part1_inflation_analysis.ipynb` | Main notebook with data cleaning, calculations, and plots |
| `data/processed/CPI_Percent_Change_Final.csv` | Final tidy dataset with % change since Jan 2020 |
| `data/raw/` | Original BLS downloads (not tracked in Git) |
| `figures/` | PNG charts (Food, Gas, Shelter, CA vs US, combined) |
| `docs/project-notes.md` | Project purpose, tools, series IDs |
| `docs/part1-insights.md` | Academic-style insights and implications |
| `docs/prediction-notes.md` | Hypotheses for inflation drivers and future modeling |
| `requirements.txt` | Python dependencies |
| `.gitignore` | Keeps raw/large files out |

---

## Highlights (Part 1)
- CPI-U (NSA) data, Jan 2020 – present.
- % change from Jan 2020 baseline.
- Clear category comparisons: Food vs. Gasoline vs. Shelter.
- Regional context: Los Angeles vs. U.S. average.

---

## Key Figures

![Combined CPI](figures/combined_cpi_comparison_chart.png)

---

## Key Insights
- **Food:** Steady, cumulative climb in costs since 2020.
- **Gasoline:** Highest volatility; major 2022 spike.
- **Shelter:** Persistent upward trend; largest anchor in headline CPI.
- **California:** Consistently above national CPI, mainly due to shelter.

---

## Reproducibility
Install requirements and run notebook:

```bash
pip install -r requirements.txt
jupyter notebook
