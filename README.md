# Gold Price Forecasting Model — India

A machine learning project that predicts future gold prices in India using 16 years of real data from 2010 to 2026.


## What This Project Does

This project looks at how gold prices in India have changed every month from January 2010 to April 2026, learns the pattern, and predicts what gold prices will look like for the next 12 months.

All prices are in **Indian Rupees (₹) per 10 grams** of 24-karat gold — the standard unit used in India.



## Data

- Gold prices from **2010 to 2023** were taken from BankBazaar and ClearTax
- Gold prices from **2024 to April 2026** were downloaded live from Yahoo Finance
- The live prices were originally in US Dollars and converted to Rupees



## Model

The model I used is **Polynomial Regression**. It works by:

1. Looking at 16 years of monthly gold prices
2. Learning the trend — gold generally goes up over time
3. Learning the seasonal pattern — gold prices rise during festivals like Diwali and Akshaya Tritiya
4. Using that knowledge to predict future prices

The data was split into:
- **Training set (80%)** 
- **Test set (20%)** 



## Results

The model achieved:
- **MAPE (average error %)** — around 4 to 6% which is considered good for financial data
- **R²** — above 0.95 meaning the model explains over 95% of price movement



## Output Charts

### Chart 1 — Gold Price History (2010 to 2026)
<img width="2382" height="728" alt="raw_gold_inr" src="https://github.com/user-attachments/assets/e0d36a08-be1c-42ed-a473-51151c109d8a" />
<br/>

This chart shows the full journey of gold prices in India over 16 years.
You can clearly see:
- Prices were around ₹18,500 in 2010
- A big jump during COVID in 2020
- A sharp rise from 2024 onwards reaching ₹1,55,000 by April 2026
- Key events like global economic crises are marked on the chart



### Chart 2 — Actual vs Predicted Prices
<img width="2382" height="880" alt="actual_vs_predicted_INR" src="https://github.com/user-attachments/assets/99185824-bb81-4569-8c4c-9b8c13fbe2f7" />

<br/>

As you can see that this chart compares what gold prices actually were versus what the model predicted.
- **Blue line** — the real gold price
- **Orange dashed line** — the model's prediction on training data
- **Red dashed line** — the model's prediction on test data it had never seen before

The closer the red line is to the blue line, the more accurate the model is.



### Chart 3 — Error Analysis (Residuals)
<img width="2384" height="732" alt="residuals_INR" src="https://github.com/user-attachments/assets/355340cc-bd4f-4512-8665-5e1d5996590a" />

<br/>

The above chart shows how far off the model was each month.
- **Blue bars** — months where the model predicted lower than actual (under-predicted)
- **Red bars** — months where the model predicted higher than actual (over-predicted)
- The histogram on the right shows most errors are small and centered around zero
which means the model is not consistently wrong in one direction



### Chart 4 — 12 Month Future Forecast
<img width="2376" height="880" alt="future_forecast_INR" src="https://github.com/user-attachments/assets/555d7455-fe62-4950-bf41-df0c827ccdf8" />

<br/>

Final Result
- **Blue line** — the last 24 months of real gold prices
- **Gold dashed line** — the predicted prices for the next 12 months
- **Shaded band** — a ±5% confidence range showing the upper and lower bounds of the forecast

The forecast gives a month by month predicted price so you can see where gold prices are expected to go over the coming year.


## Author

**VINEETHA**
