# 🕒 Time Series Analysis for Food Delivery

This project analyzes hourly food delivery order data using time series models including ETS, ARIMA, LSTM, and BiLSTM. The goal is to build and compare predictive models to forecast future order volumes based on historical patterns.

## 📁 Dataset

The dataset used is `orders_autumn_2020.csv`, which contains timestamps for each food delivery order during autumn 2020.

### Sample Features:
- `TIMESTAMP`: Datetime of the order (used for resampling by hour)

## 📊 Workflow Overview

### 1. **Data Preprocessing**
- Convert timestamps to datetime format
- Resample data by hour to count orders
- Fill missing hours with zero orders

### 2. **Visualization & Decomposition**
- Plot hourly order volume
- Decompose time series into trend, seasonality, and residuals (using seasonal decomposition)

### 3. **Train-Test Split**
- Last 168 hours (1 week) used for testing
- Remaining data used for training

### 4. **Forecasting Models**
#### 🔵 ETS (Exponential Smoothing)
- Seasonal Holt-Winters model

#### 🔵 ARIMA
- Model with seasonal order `(1,1,1,24)`

#### 🔵 LSTM
- Deep learning model using TensorFlow/Keras
- Uses past 24 hours to predict the next hour

#### 🔵 BiLSTM
- Bidirectional LSTM for improved learning of temporal context

### 5. **Evaluation**
- RMSE is used to evaluate all models
- Visualization of predictions vs. actual values

## 🧪 Results

| Model   | RMSE (Lower is Better) |
|---------|------------------------|
| ETS     | ✅ Auto-calculated      |
| ARIMA   | ✅ Auto-calculated      |
| LSTM    | ✅ Auto-calculated      |
| BiLSTM  | ✅ Auto-calculated      |

## 📦 Requirements

Install dependencies using pip:

```bash
pip install pandas numpy matplotlib seaborn statsmodels scikit-learn tensorflow
