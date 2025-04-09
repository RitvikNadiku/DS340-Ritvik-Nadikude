# Bitcoin-Price-Prediction-2025 

# Model 1
For this project, I implemented a time-series forecasting model to predict Bitcoin prices using the Seasonal AutoRegressive Integrated Moving Average (SARIMA) model. I sourced the dataset from Investing.com on February 12, 2025, and used it to forecast Bitcoin prices up to March 13, 2025.

## Data Preprocessing:
1. I loaded and cleaned the dataset, renaming columns for clarity.
2. I converted the date column to datetime format and transformed the price values into numerical data.
3. I sorted the data in ascending order to ensure proper time-series analysis.
   
## Model Training:
1. I trained a SARIMA model on historical Bitcoin prices up to February 12, 2025.
2. I set the model parameters as (2,1,2) for ARIMA order and (1,1,1,12) for seasonal adjustments to capture trends and seasonality.
   
## Forecasting Future Prices:
Using the trained SARIMA model, I predicted Bitcoin prices for the next 30 days (Feb 13 – March 13, 2025). I stored the predictions in a DataFrame with their corresponding dates.

## Model Performance and Prediction Strategy:
Since this model works better for short-term price predictions than long-term forecasts, I decided to focus on monthly and weekly predictions rather than extended periods.

## Visualization:
1. I created a line chart to visualize historical Bitcoin prices alongside the predicted values.
2. The plot highlights trends and provides insights into potential future movements.

# Model 2: Enhanced Bitcoin Price Prediction with Trading Strategies

For the advanced phase of this project, I developed an enhanced prediction system (Model 2) that builds upon Model 1 by incorporating trading volume data and implementing trading strategy recommendations. I sourced updated Bitcoin data through March 30, 2025, and used it to forecast both price and volume for April 2025, while providing actionable trading insights.

## Data Preprocessing:
1. I loaded and cleaned the dataset, maintaining the same column structure as Model 1.
2. I converted date fields to datetime format and transformed price values into numerical data.
3. I processed volume data by converting "K" notations to thousands for proper numerical analysis.
4. I sorted data chronologically to ensure proper time-series analysis.

## Dual-Model Training:
1. I implemented parallel SARIMA models - one for price prediction and one for volume prediction.
2. Both models maintained the parameters (2,1,2)(1,1,1,12) established in Model 1.
3. I trained both models on historical data through March 30, 2025.

## Trading Strategy Implementation:
1. I developed an algorithm to determine optimal position styles (Long or Short) based on volume trends.
2. The system identifies entry points by analyzing the minimum price within the previous 7-day period.
3. The model recommends Long positions when recent volume exceeds the 7-day average, and Short positions otherwise.

## Profit & Loss Analysis:
1. I integrated daily P&L calculations to quantify potential returns for each recommended strategy.
2. For Long positions, P&L is calculated as the difference between predicted price and entry price.
3. For Short positions, P&L is calculated as the difference between entry price and predicted price.

## Forecasting & Visualization:
1. The model generates 30-day forecasts for both price and volume simultaneously.
2. I created dual-axis visualizations showing historical and predicted values for both metrics.
3. The system displays daily P&L projections to help identify optimal exit points.

## Model Performance:
As shown in the output comparison, Model 2 achieved high accuracy for short-term predictions, with forecasted prices closely matching actual values for the first few days of April 2025. For example, on April 1, the predicted price ($83,939) was within 1.5% of the actual price ($82,525). However, market volatility after April 5 led to growing discrepancies, reinforcing the need for the 2-4 day retraining protocol recommended in this implementation.

The enhanced Model 2 provides a complete trading framework that not only predicts Bitcoin's price movement but offers actionable strategies to capitalize on these predictions through optimal entry and exit points.


