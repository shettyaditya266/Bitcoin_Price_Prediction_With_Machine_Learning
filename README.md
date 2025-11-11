# 📈 Bitcoin Price Prediction using Machine Learning (Python + Jupyter Notebook)

This project builds a complete **Bitcoin price prediction system** using historical OHLCV data.  
It includes:

- Data cleaning & preprocessing
- Timestamp correction (scientific notation → datetime)
- Resampling 1-minute data to hourly data
- Exploratory Data Analysis (EDA) visualizations
- Feature engineering (lags, rolling windows)
- Machine learning model training (Ridge Regression)
- Model evaluation with visualizations
- Next-hour Bitcoin price forecasting

The project is implemented entirely in **Python** using **Pandas, NumPy, scikit-learn, and Matplotlib**.

---

## ✅ Project Overview

This model predicts the **next-hour Bitcoin closing price** using engineered time-series features.

Steps included:

1. Load & clean raw 1-minute BTC data  
2. Convert scientific-notation timestamp (e.g., `1.33E+09`) into datetime  
3. Set timestamp as a `DatetimeIndex`  
4. Resample to hourly OHLCV  
5. Visualize historical behavior  
6. Build lag-based supervised ML features  
7. Train a regression model  
8. Evaluate predictions  
9. Forecast the next-hour BTC price  

---

## ✅ Dataset

The project uses a CSV file with the following columns:


✅ Timestamp Format  
The `Timestamp` column is in **Unix time (seconds)** but stored in scientific notation (e.g., `1.33E+09`).  
We convert it using:

```python
df["Timestamp"] = pd.to_datetime(df["Timestamp"].astype(float), unit="s")

## ✅ Key Features
✅ 1. Timestamp Fixing

The raw timestamp is stored in scientific notation; we convert it reliably using Pandas.

✅ 2. Hourly Resampling

The 1-minute data is resampled to hourly data for stable modeling.

✅ 3. Before-Model Visualizations

Minute-level BTC price

Hourly BTC close price

24-hour moving average

Hourly returns distribution

✅ 4. Feature Engineering

Created features include:

Lag features: Close(t-1) to Close(t-24)

Rolling means: 6-hour, 24-hour

Rolling standard deviations

Volume

These turn time series into supervised ML format.

✅ 5. Model

We use Ridge Regression due to speed, stability, and explainability:

model = Ridge(alpha=5.0)

✅ 6. Model Evaluation

We evaluate using:

MAE (Mean Absolute Error)

RMSE (Root Mean Squared Error)

Actual vs Predicted plot

Residual plot

Predicted vs Actual scatter plot

✅ 7. Next-Hour Forecast

The model predicts the next-hour BTC closing price using the latest available data.
