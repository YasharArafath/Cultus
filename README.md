# Advanced Time Series Forecasting with Prophet and Model Stacking

This project focuses on implementing and comparing advanced time series forecasting techniques by combining a modern **probabilistic model (Facebook Prophet)** with a **traditional statistical model (SARIMAX)** and a **machine learning model (LightGBM)** into a **stacking ensemble** architecture.

The main objective is to achieve **superior predictive accuracy** and provide robust **uncertainty quantification** (prediction intervals) compared to using the individual models alone.

## 🛠️ Key Components and Requirements

### 1. Data Generation
* Programmatically generate a **complex, synthetic time series dataset** of at least **3 years of hourly data**.
* The dataset must incorporate:
    * A **non-linear trend**.
    * Multiple seasonality patterns (at least **daily** and **weekly/yearly**).
    * Realistic **noise and outliers**.

### 2. Model Implementation
* Implement and tune **three base forecasting models**:
    * **Facebook Prophet**
    * **SARIMAX**
    * **LightGBM** (trained on time-based features).

### 3. Stacking Ensemble Design
* Design and implement a **time-series-aware stacking ensemble**.
* The predictions from the three base models will serve as the **input features** for a **meta-regressor** (e.g., Ridge Regression or a simple Neural Network).

### 4. Rigorous Evaluation
* Conduct **time series cross-validation** (e.g., rolling window validation) for tuning and evaluation.
* Evaluate the performance of both the individual base models and the final stacked ensemble using metrics like **MAE, RMSE, and WAPE**.

### 5. Uncertainty Quantification
* Generate and document **$90\%$ prediction intervals** for the final **30-day forecast** provided by the stacked model.

Sure! Here's your data formatted as a clean table:

| Model                                           | MAE  | RMSE | WAPE |
| ----------------------------------------------- | ---- | ---- | ---- |
| Prophet                                         | 40.0 | 48.0 | 8.0% |
| SARIMAX                                         | 45.0 | 55.0 | 9.0% |
| LightGBM                                        | 35.0 | 42.0 | 7.0% |
| Stacked Ensemble (Prophet + SARIMAX + LightGBM) | 32.0 | 38.5 | 6.4% |


