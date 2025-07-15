# Bikeshare Demand Forecasting with Prophet and XGBoost
This project forecasts **hourly bikeshare demand** by integrating a **hybrid time series approach** combining [Facebook Prophet](https://facebook.github.io/prophet/) and XGBoost. The model leverages temporal signals and real-time weather features such as temperature, wind speed, humidity, and precipitation to improve forecast accuracy.

## Model Overview
- **Prophet**: Captures seasonality, trend, and holiday effects
- **XGBoost**: Learns patterns from Prophet’s residuals and engineered features
- **Hybrid Output**: Combines the strengths of statistical and machine learning models to enhance accuracy

## Key Features
- Trained on **over 10 million records** of bikeshare and weather data
- Integrated **lag features** and **residual learning**
- Forecasts hourly demand with **R² of 0.89**, a 15% improvement over Prophet alone
- Designed for **real-time operational deployment**
  
## Files Included
- `Bikeshare.ipynb`: Main notebook implementing the hybrid forecasting model
- `Weather_data.rar`: Weather data used for model training (temperature, humidity, etc.)
- Capital Bikeshare trip data is sourced from:  [https://s3.amazonaws.com/capitalbikeshare-data/index.html](https://s3.amazonaws.com/capitalbikeshare-data/index.html)

## How It Works
1. Load and preprocess demand and weather data
2. Train a **Prophet** model on historical ride counts and weather regressors
3. Compute residuals and pass them to an **XGBoost** model with lagged features
4. Combine predictions from both models to forecast future demand

## Running the Notebook
1. Extract `Weather_data.rar`  
2. Run `Bikeshare.ipynb` step-by-step  
   Ensure that demand data is downloaded from the provided link and preprocessed accordingly

## Future Work
- Integrate weather forecasts via OpenWeatherMap API
- Extend to multi-day forecasts and other cities
- Deploy as a real-time dashboard using Streamlit or Flask

> This project was born out of a personal goal to build a **real-time, practically usable time series forecasting model**. By combining statistical modeling with machine learning, it demonstrates how hybrid approaches can drive smarter, data-informed decisions in urban mobility systems like bikeshare networks.
