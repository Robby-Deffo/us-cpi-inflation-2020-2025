# Data Dictionary — CPI_Percent_Change_Final.csv

## Overview

This file is the primary processed dataset for the U.S. CPI Inflation Analysis project. It contains monthly cumulative percent changes for four BLS CPI series, all indexed to **January 2020 = 0%**.

**File location:** `data/processed/CPI_Percent_Change_Final.csv`  
**Rows:** 65 (monthly observations, Jan 2020 – mid 2025)  
**Columns:** 5

---

## Column Definitions

| Column | Type | Unit | Description |
|---|---|---|---|
| `Date` | String (YYYY-MM-DD) | — | First day of each month; represents that month's CPI reading |
| `Food_CPI % Chnge` | Float | Percent (%) | Cumulative % change in U.S. Food & Beverages CPI since Jan 2020 |
| `Gasoline_CPI % Chnge` | Float | Percent (%) | Cumulative % change in U.S. Gasoline (All Types) CPI since Jan 2020 |
| `Shelter_CPI % Chnge` | Float | Percent (%) | Cumulative % change in U.S. Shelter CPI since Jan 2020 |
| `Cali_CPI % Chnge` | Float | Percent (%) | Cumulative % change in Los Angeles–Long Beach–Anaheim metro All-Items CPI since Jan 2020 |

---

## Baseline Convention

All values in this file represent **cumulative percent change from January 2020**:

- January 2020 row: all four columns = `0.0`
- A value of `15.75` means prices in that category were 15.75% higher than in January 2020
- Negative values (present in the Gasoline series in 2020) indicate prices fell below the baseline

---

## Source Series (BLS)

| Column | BLS Series ID | Survey | Adjustment |
|---|---|---|---|
| Food | `CUUR0000SAF` | CPI-U | Not Seasonally Adjusted |
| Gasoline | `CUUR0000SETB01` | CPI-U | Not Seasonally Adjusted |
| Shelter | `CUUR0000SAH1` | CPI-U | Not Seasonally Adjusted |
| California / LA | `CUURS49ASA0` | CPI-U | Not Seasonally Adjusted |

Raw source files are stored in `data/raw/` (not tracked in Git due to file size and reproducibility via BLS Data Finder).

---

## Derivation Formula

Each percent-change column was computed in Python (Pandas) as:

```python
df[col + '_pct'] = ((df[col] - df[col].iloc[0]) / df[col].iloc[0]) * 100
```

Where `df[col].iloc[0]` is the January 2020 value for that series.

---

## Notes

- Data is **Not Seasonally Adjusted (NSA)**. Month-to-month fluctuations may reflect seasonal patterns in addition to trend inflation.
- The California series (`CUURS49ASA0`) covers the **Los Angeles–Long Beach–Anaheim** Combined Statistical Area — it is an all-items index, not a category-specific one, and therefore is not directly comparable to the national category series.
- Raw BLS files can be re-downloaded at [https://www.bls.gov/cpi/](https://www.bls.gov/cpi/) using the Series IDs above.
