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

