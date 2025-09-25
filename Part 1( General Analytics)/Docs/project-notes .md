# Project Notes – CPI Inflation Analysis

## Purpose
This project investigates inflation trends in the U.S. from **January 2020 onward** using CPI-U (Not Seasonally Adjusted) data. It focuses on three essential categories—**Food**, **Gasoline**, and **Shelter**—and provides a California (LA metro) comparison. The goal is to build reproducible code, visualizations, and insights that communicate both the magnitude and persistence of inflation.

## Data Source
- **Bureau of Labor Statistics (BLS)**
- **CPI-U (All Urban Consumers), Not Seasonally Adjusted**
- Retrieved via BLS Data Finder (https://www.bls.gov/cpi/)

## Series IDs (examples)
- Food & Beverages (CUUR0000SAF)
- Gasoline, All Types (CUUR0000SETB01)
- Shelter (CUUR0000SAH1)
- All Items, Los Angeles Metro (CUURS49ASA0)

## Methodology
- Baseline: **January 2020 = 100%**
- Computed % change since baseline:  
  \[
  \text{PctChange} = \frac{Value_t - Value_{Jan2020}}{Value_{Jan2020}} \times 100
  \]
- Data wrangled in Python with Pandas, output cleaned CSV for visualization.
- Visualization: Matplotlib, Seaborn, Plotly.

## Outputs
- Clean dataset (`data/processed/CPI_Percent_Change_Final.csv`)
- Charts in `figures/`
