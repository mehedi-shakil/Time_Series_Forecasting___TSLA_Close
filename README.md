# Time-Series Forecasting for Tesla Stock Prices (TSLA)

This project aims to forecast Tesla (TSLA) stock prices using **ARIMA** (AutoRegressive Integrated Moving Average) and **LSTM** (Long Short-Term Memory) models. We compare the performance of traditional statistical models and deep learning models in predicting future stock prices.

## Project Overview
We use daily closing prices of Tesla (TSLA) from 2010–2025 to compare three forecasting models:
- **Naive Baseline**: The price from the previous day is used as the prediction for the next day.
- **ARIMA Model**: A traditional statistical model that captures linear patterns in the time series data.
- **LSTM Model**: A deep learning model capable of capturing complex non-linear dependencies and patterns in stock price movements.

### Evaluation
The models were evaluated using a **rolling walk-forward validation strategy**. The evaluation metrics used are:
- **RMSE (Root Mean Square Error)**
- **MAPE (Mean Absolute Percentage Error)**

### Results

| Model                | Validation RMSE | Validation MAPE | Test RMSE | Test MAPE |
|----------------------|-----------------|------------------|-----------|-----------|
| Naive (t-1)          | 10.11           | 2.90%            | 8.84      | 2.77%     |
| ARIMA (walk-forward) | 10.28           | 2.98%            | 8.85      | 2.77%     |
| LSTM (returns → price) | 10.11         | 2.89%            | 8.83      | 2.76%     |

### Conclusion
The **LSTM** model generalized the best, providing slight but consistent improvements over both the ARIMA and Naive baseline models. This suggests that while traditional statistical models like ARIMA perform well for stock prices, deep learning models like LSTM can capture more complex patterns, resulting in better forecasting accuracy.

---

## Files
- **`Time_Series_Forecasting_—_TSLA_Close.ipynb`**: The main code notebook for data preprocessing, model training, and forecasting.
- **`arima.joblib`**: The trained ARIMA model.
- **`lstm.keras`**: The trained LSTM model.
- **`Time_Series_Forecasting___TSLA_Close.pdf`**: The project report.

---

## Installation

### Dependencies
To run the notebook, you will need the following libraries:
```bash
pip install numpy pandas matplotlib tensorflow scikit-learn statsmodels joblib
