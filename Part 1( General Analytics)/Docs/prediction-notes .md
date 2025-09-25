# Prediction Notes – Inflation Drivers (Hypotheses)

This document outlines hypotheses for what drives inflation dynamics, to inform future predictive modeling.

## Hypotheses
1. **Gasoline prices** (oil shocks, geopolitical events) will continue to dominate short-term CPI volatility.
2. **Shelter inflation** will remain sticky due to lease lags and structural housing shortages.
3. **Food inflation** will track both global commodity prices and supply chain pressures, rising steadily rather than spiking.
4. **Interest rate hikes** (Fed Funds) will dampen demand-side components but only gradually slow shelter inflation.
5. **Regional variation** will persist, with higher-cost metros (e.g., CA, NY) experiencing above-average CPI growth.

## Possible Modeling Approaches
- **Multiple Linear Regression:** CPI ~ interest rates + unemployment + oil + M2 + consumer confidence.
- **Time Series Models:** ARIMA/SARIMA for category-level forecasting.
- **ML Approaches:** Random Forest, Gradient Boosted Trees for feature importance and non-linear effects.

## Next Steps
- Collect macroeconomic indicators from FRED (rates, unemployment, M2).
- Merge with CPI categories for 2020–present.
- Test baseline regression, evaluate R² and residuals.
