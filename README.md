# Ecuador Store Sales Forecasting Project (Data form Kaggle)

This project focuses on forecasting daily product family sales for 54 retail stores in Ecuador. The dataset includes sales history, promotions, oil prices, holidays, and transactional data. The goal is to accurately predict future sales from August 16 to 31, 2017.

---

## Project Objective

- Predict future sales for each **product family** across **multiple stores**.
- Incorporate **external factors** (holidays, promotions, oil prices) to improve accuracy.
- Use this project as a showcase of time series forecasting and feature engineering capabilities.

---

## Dataset Overview

- **Source**: Kaggle (Corporación Favorita Grocery Sales Forecasting)
- **Files Used**:
  - `train.csv` – daily sales records
  - `test.csv` – test set for the final submission
  - `stores.csv` – store metadata
  - `transactions.csv` – transaction volume per store
  - `holidays_events.csv` – national/local events
  - `oil.csv` – crude oil price (as economic proxy)

---

## Key Steps

### 1. Exploratory Data Analysis (EDA)
- Visualized daily sales patterns by product family and store
- Analyzed the impact of holidays and oil price on sales behavior

### 2. Feature Engineering
- Extracted date-related features (weekday, month, holiday flags)
- Integrated external datasets (e.g., oil price smoothed, promotional effects)

### 3. Modeling
- Utilized **LightGBM** and **XGBoost** for time-aware regression
- Applied mean encoding, lag features, and rolling statistics for accuracy

### 4. Evaluation
- Forecasts evaluated using **Root Mean Squared Log Error (RMSLE)**
- Visual inspection of over/under-prediction trends

---

## Results & Insights

- Strong weekly seasonality observed (especially weekends and paydays)
- Promotions and holidays significantly affected short-term demand
- Oil price acted as a macroeconomic proxy influencing sales

> Forecast performance was improved with targeted lag/rolling features and holiday-aware modeling.

---

## Technologies Used

- Python, Pandas, NumPy
- Matplotlib, Seaborn for Visualization
- Scikit-learn, LightGBM, XGBoost
- Jupyter Notebook / Google Colab
