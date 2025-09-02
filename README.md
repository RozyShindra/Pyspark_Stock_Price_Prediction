# Stock Market Price Prediction using PySpark & yFinance

## Project Overview

This project focuses on predicting stock market **closing prices** using historical market data and machine learning models. By leveraging **PySpark** for large-scale data processing and **Yahoo Finance API** (`yFinance`) for fetching real-time stock data, this system can efficiently handle and process financial time series data for accurate forecasting.

Stock price prediction is crucial for:
- Retail and institutional investors
- Portfolio managers
- Algorithmic trading systems
- Financial research & analytics

Combining distributed computing and machine learning allows us to build **scalable, fast, and interpretable prediction pipelines**.

---

## Problem Statement

Despite the abundance of financial data, accurately predicting stock prices remains challenging due to:
- Market volatility and noise
- Influence of global events
- Seasonal and temporal effects

Most traditional models fail to integrate large-scale time-dependent features efficiently. Additionally, user-friendly solutions allowing **flexible model training for custom companies and periods** are rare.

---

## Proposed Approach

This project implements a **step-by-step prediction pipeline** for forecasting stock closing prices:

### Key Steps:

1. **User Interaction**
   - Prompt user to select a company from top 10 stocks (e.g., AAPL, MSFT, GOOGL).
   - Let user choose the time period (e.g., 1y, 5y, max).

2. **Data Collection**
   - Download historical data using `yFinance` for the selected company.

3. **Feature Engineering**
   - Moving averages (20, 50, 200 days)
   - Daily returns and volatility
   - Price change, gain/loss indicators

4. **Visualization**
   - Plot raw prices and technical indicators.
   - Compare actual vs predicted values.

5. **Model Training**
   - Use PySpark’s `RandomForestRegressor` and `GBTRegressor` to predict future prices.
   - Split data into train/test sets with reproducibility.

6. **Evaluation**
   - Report RMSE for each model.
   - Plot predicted vs actual prices.

     <img width="1005" height="547" alt="image" src="https://github.com/user-attachments/assets/3cfa4ecd-8d8b-4e59-beab-a7da3433e719" />
     <img width="1005" height="547" alt="image" src="https://github.com/user-attachments/assets/64d8ddbe-dfa1-4b8a-af4b-88f05834f689" />



---

## Future Scope

This project lays the foundation for a **fully automated stock forecasting platform**. It can be scaled in several directions:

1. **Automated ML System**
   - Build a UI (e.g., using Streamlit or Flask) where users input:
     - Company name/symbol
     - Start and end date for model training
     - Desired prediction date(s)

2. **Model Optimization**
   - Integrate hyperparameter tuning (e.g., grid search, Bayesian optimization).
   - Support additional models like XGBoost, LSTM (with Spark MLlib or external interfaces).

3. **Multiple Stock Portfolio Analysis**
   - Predict and compare returns across multiple companies.
   - Support portfolio-level visualization and optimization.

4. **Real-Time Deployment**
   - Deploy the trained models as REST APIs.
   - Schedule daily predictions using cron jobs or streaming data via Kafka.

---


