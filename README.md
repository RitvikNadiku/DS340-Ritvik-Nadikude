# Bitcoin-Price-Prediction-2025

For this project, I implemented a time-series forecasting model to predict Bitcoin prices using the Seasonal AutoRegressive Integrated Moving Average (SARIMA) model. I sourced the dataset from Investing.com on February 12, 2025, and used it to forecast Bitcoin prices up to March 13, 2025.

# Data Preprocessing:
1. I loaded and cleaned the dataset, renaming columns for clarity.
2. I converted the date column to datetime format and transformed the price values into numerical data.
3. I sorted the data in ascending order to ensure proper time-series analysis.
   
# Model Training:
1. I trained a SARIMA model on historical Bitcoin prices up to February 12, 2025.
2. I set the model parameters as (2,1,2) for ARIMA order and (1,1,1,12) for seasonal adjustments to capture trends and seasonality.
   
# Forecasting Future Prices:
Using the trained SARIMA model, I predicted Bitcoin prices for the next 30 days (Feb 13 – March 13, 2025). I stored the predictions in a DataFrame with their corresponding dates.

# Model Performance and Prediction Strategy:
Since this model works better for short-term price predictions than long-term forecasts, I decided to focus on monthly and weekly predictions rather than extended periods.

# Visualization:
1. I created a line chart to visualize historical Bitcoin prices alongside the predicted values.
2. The plot highlights trends and provides insights into potential future movements.


