# Apple-Stock-Price-Prediction---Time-Series-Machine-Learning
This project helps predict Apple’s future stock prices by learning patterns from past market data, helping investors understand trends and make informed decisions.

# Apple Stock Price Prediction & Forecasting System

## Overview
This project presents an end-to-end **time-series forecasting system** for predicting **Apple Inc. (AAPL) stock prices** using historical market data. The solution combines **statistical models, machine learning, and deep learning techniques** to analyze trends, volatility, and seasonality, followed by rigorous model evaluation and deployment.

The final system is deployed as a **production-ready Streamlit web application**, enabling users to generate future stock price forecasts with interactive visualizations.

---

## Business Problem
Stock markets are highly volatile and influenced by multiple factors such as historical price movement, market trends, and economic conditions. Traditional linear models often fail to generalize well under market fluctuations.

This project addresses the problem of:
- Identifying the most suitable forecasting approach for volatile stock data
- Producing accurate short-term forecasts
- Delivering predictions through an accessible, real-world application

---

## Objectives
- Perform in-depth analysis of Apple stock prices from **2012 to 2019**
- Study **trend, volatility, and seasonality patterns**
- Build and compare multiple forecasting models
- Select the best-performing model using statistical metrics
- Forecast **future stock prices for the next 90 trading days**
- Deploy the model as an interactive web application

---

## Dataset
- **Source:** Yahoo Finance  
- **Time Period:** 2012 – 2019  
- **Granularity:** Daily stock prices  
- **Features:**
  - Open
  - High
  - Low
  - Close
  - Adjusted Close
  - Volume

---

## Data Preparation
- Converted date fields to `datetime` format
- Sorted data chronologically to preserve time dependency
- Validated and handled missing or inconsistent values
- Structured dataset for time-series modeling
- Prevented data leakage by avoiding random data splits

---

## Exploratory Data Analysis
The EDA phase focused on understanding market behavior and price movement patterns:
- Long-term upward trend with short-term fluctuations
- Volatility analysis to assess market risk
- Comparative trend analysis with **S&P 500 index**
- Impact assessment of **U.S. inflation rates**
- Seasonal decomposition into trend, seasonal, and residual components
- **ADF stationarity test** confirming non-stationary behavior

---

## Modeling Approach
Multiple forecasting models were implemented and evaluated:

### ARIMA
- Captures short-term linear dependencies
- Limited effectiveness during high volatility periods

### SARIMA
- Incorporates seasonality into ARIMA
- Provides improved stability but limited adaptability

### LSTM
- Deep learning model for long-term dependencies
- Exhibited overfitting on unseen data

### XGBoost (Final Model)
- Machine learning regression model
- Effectively captures non-linear patterns
- Demonstrated superior generalization and robustness

---

## Model Evaluation
Models were evaluated using industry-standard metrics:
- RMSE
- MAE
- MSE
- R² Score

### Final Results
| Model    | Performance Summary |
|---------|---------------------|
| ARIMA   | Captured trend, weak during volatility |
| SARIMA | Stable but limited improvement |
| LSTM   | Overfitting observed |
| **XGBoost** | **Best overall performance** |

- **Selected Model:** XGBoost  
- **R² Score:** 0.83  
- Demonstrated strong predictive accuracy on unseen data

---

## Forecasting
- Generated **30-day future stock price forecasts**
- Used recursive forecasting methodology
- Predictions presented in both tabular and graphical formats

---

## Deployment Architecture
- **Backend:** Python-based prediction engine
- **Model Serialization:** Pickle
- **Frontend:** Streamlit
- **Features:**
  - User-defined forecast horizon
  - Interactive charts
  - Clean and intuitive UI

🔗 **Live Application:**  
https://stock-price-forecast-app-murjpbg37umbrwjz2txkre.streamlit.app/

---

## Technology Stack
- Python
- Pandas, NumPy
- Matplotlib
- Statsmodels (ARIMA, SARIMA)
- XGBoost
- TensorFlow / Keras (LSTM)
- Streamlit

---

## Challenges & Solutions
- **Non-stationary data:** Addressed through decomposition and stationarity testing
- **Model overfitting:** Detected via train-test performance comparison
- **Data leakage risk:** Prevented by time-aware splitting
- **Model selection:** Solved using metric-driven evaluation
- **Deployment compatibility:** Managed environment and version constraints

---

## Key Outcomes
- Identified **XGBoost** as the most reliable model for volatile stock data
- Achieved strong generalization with **R² = 0.83**
- Delivered a fully deployed, user-friendly forecasting application

---

## Team & Mentorship
**Mentor:** Sadiya Naaz Ansari  

**Team Members:**  
Akanksha Kishorrao Amale, Niharika Hibare, 
Vanama Akhila, Charan Kumar S, Aswin N S, 
Goroji Ramanjaneyulu, Ummagoni Priyanka

---

## Conclusion
This project demonstrates a complete **data science lifecycle**—from exploratory analysis and model development to evaluation and deployment. The final system provides reliable stock price forecasts and serves as a scalable foundation for real-world financial analytics applications.

---

