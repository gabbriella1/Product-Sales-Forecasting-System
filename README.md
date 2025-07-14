# Product-Sales-Forecasting-System

This project presents a machine learning approach to **time series forecasting** using **XGBoost** for product sales at a Dutch consumer goods company.

## Objective

To build a forecasting system that predicts daily sales quantities for individual products using historical order data.

---

## Key Features

- Built using Python, Pandas, and XGBoost
- Time series modeling per product (by `ProductCode`)
- Feature engineering:
  - Lag features (`lag_1`, `lag_7`, `lag_30`)
  - Rolling means and standard deviations
  - Percent change and rolling diffs
  - Temporal signals (`month`, `dayofweek`, etc.)
- Outlier clipping for sales spikes
- Evaluation using RMSE, MAE, and R² metrics

---

## Sample Data

Due to a Non-Disclosure Agreement (NDA) with the data provider:

- Product codes (`random_codes`) have been anonymized as `"sampleOfProductCodes"`  
- The dataset file path is set to `"sample_data.csv"`  
- All product identifiers in plots have been visually masked  

---

## Model Results

### Example 1 – 
- **Train Set**  
  `RMSE: 0.19`, `MAE: 0.11`, `R²: 1.0000`
- **Test Set**  
  `RMSE: 12.22`, `MAE: 7.60`, `R²: 0.9786`

![Forecast vs. Actual - Product B](/Forecast%20vs.%20Actual%20for%20ProductCode%20B.png)

---

### Example 2 –
- **Train Set**  
  `RMSE: 0.08`, `MAE: 0.03`, `R²: 1.0000`
- **Test Set**  
  `RMSE: 0.91`, `MAE: 0.36`, `R²: 0.9847`

![Forecast vs. Actual - Product A](/Forecast%20vs.%20Actual%20for%20ProductCode%20A.png)


## Google Trends Integration

- Used `pytrends` to extract interest over time for relevant keywords
- Normalized on a 0–100 scale (Google Trends)
- Weekly resolution, filtered for the Netherlands
- Helped enrich data

---

## Future Improvements

- Integrate additional external data sources 
- Plan to connect the forecasting system with a Large Language Model (LLM) to enable a conversational interface. 

---


