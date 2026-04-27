# Gold Price Forecasting Model — India (INR)

A machine learning project that forecasts 24-karat gold prices in India
(₹ per 10 grams) using 16 years of historical data (2010–2026) and
Polynomial Regression with Fourier seasonal features.

---

## Project Overview

| Item | Detail |
|---|---|
| Currency | Indian Rupee (₹) per 10 grams |
| Gold type | 24-karat (999 purity) |
| Data range | January 2010 – April 2026 |
| Frequency | Monthly |
| Model | Polynomial Regression (degree=2) with Fourier features |
| Train / Test split | 80% / 20% |
| Forecast horizon | 12 months ahead |

---

## Data Sources

| Period | Source | Method |
|---|---|---|
| 2010–2023 | BankBazaar / ClearTax (MCX-referenced annual averages) | Verified and hardcoded |
| 2024–2026 | Yahoo Finance — GC=F (USD/oz) × USDINR=X | Auto-fetched and converted to ₹/10g |

The conversion formula used:  
`Price (₹/10g) = Gold_USD × USD_INR × 10 / 31.1035`  
where 31.1035 is the number of grams in one troy ounce.

---

## Features Used in the Model

| Feature | Description |
|---|---|
| t | Time index (0, 1, 2, ...) — captures linear trend |
| t² | Squared time — captures accelerating/curved growth |
| sin1, cos1 | Fourier pair — 12-month seasonal cycle |
| sin2, cos2 | Fourier pair — 6-month seasonal sub-cycle |
| ma3 | 3-month moving average — short-term momentum |
| ma6 | 6-month moving average — medium-term momentum |
| ma12 | 12-month moving average — long-term trend |

---

## Model Performance (Test Set)

| Metric | Description | Value |
|---|---|---|
| MAE | Average rupee error per month | ₹ — (run notebook to see) |
| RMSE | Root mean squared error | ₹ — (run notebook to see) |
| MAPE | Mean absolute percentage error | — % (run notebook to see) |
| R² (train) | Variance explained on training data | — (run notebook to see) |

---

## Output Charts

| File | Description |
|---|---|
| raw_gold_inr.png | Full historical price trend 2010–2026 with event annotations |
| actual_vs_predicted_INR.png | Actual vs predicted prices across train and test periods |
| residuals_INR.png | Monthly residual errors (bar chart + distribution histogram) |
| future_forecast_INR.png | 12-month forecast with ±5% confidence band |

---


## Author

**VINEETHA**  



