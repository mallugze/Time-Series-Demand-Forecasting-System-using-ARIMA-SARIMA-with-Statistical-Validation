# 📈 Time-Series Demand Forecasting System
An end-to-end statistical modeling project for predicting retail inventory demand using ARIMA and SARIMA architectures.

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Statsmodels](https://img.shields.io/badge/Statsmodels-Analysis-blue?logo=statsmodels)
![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458?logo=pandas)
![Status](https://img.shields.io/badge/Project-Completed-success)
![Environment](https://img.shields.io/badge/Environment-Google_Colab-orange?logo=googlecolab)

## 📌 Overview
This project focuses on forecasting daily sales for a retail store ("Store 40") across specific product families. By analyzing historical trends and seasonality, the system provides 30-day future sales projections to optimize supply chain management.

## 🚀 Key Highlights
* **Statistical Validation:** Performed **Augmented Dickey-Fuller (ADF)** tests to ensure data stationarity before modeling (p-value: 0.00013).
* **Feature Analysis:** Utilized **Rolling Statistics (Mean & Std)** and **ACF/PACF plots** to identify optimal lag parameters ($p, d, q$).
* **Model Comparison:** Evaluated multiple configurations ($ARIMA(1,0,0)$, $(0,0,1)$, and $(1,0,1)$) using **AIC/BIC scores** to find the most efficient fit.
* **Residual Diagnostics:** Conducted error analysis to ensure model residuals resembled "White Noise," confirming that all patterns were captured.
* **Forecast Visualization:** Generated a 30-day forecast with **95% Confidence Intervals** to account for uncertainty.

## 🛠 Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Statsmodels (Time-Series Analysis)
* **Visualization:** Matplotlib, Seaborn

## 📊 Dataset
[Corporación Favorita Grocery Sales Forecasting](https://www.kaggle.com/c/store-sales-time-series-forecasting)
> **Note:** The analysis specifically targets "AUTOMOTIVE" sales in Store 40 to demonstrate the model's ability to handle erratic daily demand.

## 📈 Model Performance
* **AIC Score:** Achieved a significantly lower AIC (**~7923**) with the $(1,0,1)$ model compared to the baseline.
* **Confidence Bounds:** Successfully mapped the variance of future sales, providing a safety buffer for inventory planning.
* **Key Insight:** In demand forecasting, capturing the interaction between historical lags and moving averages is critical; the $(1,0,1)$ configuration significantly reduced information loss compared to simpler models.

---
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1_arNGv8Co6YARWsps8L1pu5wBw-5De1h)
