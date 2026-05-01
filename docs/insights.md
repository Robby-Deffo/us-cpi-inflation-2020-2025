# Insights — U.S. CPI Inflation Analysis (Jan 2020 – Mid 2025)

## Abstract

This analysis examines the evolution of U.S. consumer prices from January 2020 through mid-2025, focusing on three essential household cost categories: Food & Beverages, Gasoline, and Shelter. Using BLS CPI-U (Not Seasonally Adjusted) data, cumulative percentage changes relative to the January 2020 baseline were computed and visualized. A regional comparison with the Los Angeles–Long Beach–Anaheim metro area (California) is included to capture geographic variation in inflation dynamics.

The findings underscore the multi-dimensional nature of the post-pandemic inflation cycle — volatile energy prices, structurally elevated food costs, and persistently sticky shelter inflation — and carry implications for households, businesses, and policymakers alike.

---

## Methodology

- **Data:** Monthly BLS CPI-U (NSA), January 2020 – mid-2025
- **Categories analyzed:** Food & Beverages, Gasoline (All Types), Shelter, California/LA Metro (All Items)
- **Baseline normalization:** January 2020 = 0% change
- **Statistical summary:** Mean, median, 75th percentile, maximum, standard deviation
- **Correlation analysis:** Pearson correlation across all four series
- **Visualization:** Individual category line charts, combined overlay, correlation heatmap

---

## Statistical Summary

| Category | Mean | Median | 75th Pctl | Max | Std Dev |
|---|---|---|---|---|---|
| Food | 15.75% | 19.20% | 24.61% | 28.79% | 9.75 |
| Gasoline | 24.40% | 26.47% | 39.31% | 89.48% | 24.69 |
| Shelter | 12.44% | 11.35% | 21.31% | 28.37% | 9.59 |
| California | 11.28% | 13.08% | 17.60% | 23.49% | 7.79 |

---

## Findings

### Gasoline — High Volatility, Shock-Driven

Gasoline was by far the most volatile category (σ = 24.69). Prices collapsed in early 2020 as pandemic lockdowns gutted demand, falling over 25% below baseline by April 2020. From 2021 onward, prices reversed sharply as travel rebounded and supply chain disruptions tightened refinery capacity. The peak came in mid-2022 — over **89% above the January 2020 baseline** — driven largely by the Russia-Ukraine conflict and resulting crude oil supply disruptions. Prices have since partially corrected but remain elevated (~20–25% above baseline as of mid-2025).

**Key takeaway:** Gasoline is a poor long-run inflation anchor; it reflects global commodity shocks rather than domestic structural pressures.

### Food — Steady, Cumulative, Structural

Food inflation followed a more moderate but persistent trajectory (σ = 9.75). Prices barely moved in 2020, then began accelerating through 2021–2022 as supply chain bottlenecks, labor shortages, and commodity cost pass-through reached consumers. By mid-2025, grocery prices are approximately **29% above January 2020 levels** — a meaningful compression of real household purchasing power, particularly for lower-income consumers where food represents a larger share of spending.

**Key takeaway:** Food inflation reflects both supply-side shocks and structural cost pass-through. It moves more slowly than energy but compounds significantly over time.

### Shelter — Persistent, Sticky, and Still Rising

Shelter inflation is the most economically significant finding of this analysis. Unlike food and gasoline, shelter prices **never declined** across the entire observation period. The cumulative increase from January 2020 to mid-2025 exceeds **28%**, with no sign of meaningful reversal. Monthly increases were modest (often <0.5%), but their consistency produced the most durable inflationary pressure in the dataset.

This stickiness reflects structural factors: lease renewal lags, chronic housing undersupply in major metro areas, and the way Owners' Equivalent Rent (OER) is constructed in BLS methodology — which captures housing costs with a significant lag relative to actual market rents.

**Key takeaway:** Shelter is the dominant anchor of headline CPI persistence. It is largely immune to short-term monetary tightening and will remain elevated absent structural housing supply increases.

### California (LA Metro) — Above-Average, Shelter-Led

The Los Angeles metro CPI tracked consistently above the national average across the full period, reaching approximately **23.5% above baseline** by mid-2025. The high correlation with national Food CPI (r = 0.99) and Shelter CPI (r = 0.98) confirms that California's elevated inflation is not driven by unique local factors so much as an amplification of the same structural forces — compounded by the region's severe existing housing shortage and high land costs.

---

## Correlation Analysis

| Pair | Pearson r | Interpretation |
|---|---|---|
| Food ↔ Shelter | 0.97 | Both reflect persistent structural cost trends |
| Food ↔ California | 0.99 | Food inflation closely mirrors the LA basket |
| Shelter ↔ California | 0.98 | Housing costs dominate the CA metro index |
| Gasoline ↔ Food | 0.60 | Moderate; fuel costs partially pass through to food |
| Gasoline ↔ Shelter | 0.46 | Weak; energy shocks don't drive housing costs |
| Gasoline ↔ California | 0.63 | Moderate; transportation is a meaningful basket component in CA |

---

## Implications

**For Households:** Real purchasing power has eroded substantially since 2020. The combination of food (+29%) and shelter (+28%) increases — both non-discretionary spending categories — represents a structural decline in real wages for households that did not see equivalent income growth.

**For Business:** Cost planning must distinguish between volatile, mean-reverting inflation (gasoline) and structural, persistent inflation (shelter, food). Long-term contracts and supply agreements anchored to pre-2022 pricing assumptions require reassessment.

**For Monetary Policy:** The Federal Reserve's rate-hiking cycle (2022–2023) was effective at dampening demand-side components and energy prices, but its impact on shelter inflation was delayed and limited. This is consistent with the known lag structure of OER in the CPI. Monetary policy has diminishing returns against supply-constrained, inelastic spending categories.

**For Data Practice:** This project demonstrates the value of baseline indexing over raw CPI levels for communicating cumulative change, and the importance of decomposing aggregate inflation into category-level dynamics.

---

## Limitations

- Analysis covers broad BLS categories; subcategories (e.g., beef vs. dairy, electricity vs. natural gas) are not disaggregated.
- Data is not seasonally adjusted (NSA); seasonal patterns may affect month-to-month interpretation.
- Regional comparison is limited to the Los Angeles metro area; other high-cost metros (New York, San Francisco) may show different dynamics.
- External macroeconomic drivers (interest rates, M2 supply, unemployment) are not included in this phase of analysis.

---

*Data source: U.S. Bureau of Labor Statistics — CPI-U, Not Seasonally Adjusted.*  
*Author: Robby Deffo | CSUN M.S. Business Analytics*
