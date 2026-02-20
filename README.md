# Retail Radar: Walmart Sales Forecasting

## Project Description
Retail Radar is a predictive analytics project designed to forecast weekly sales for 45 Walmart locations. The project focuses on identifying the influence of macroeconomic indicators and seasonal cycles on retail volume. A key highlight of this analysis is the **"Tandem Duo"**—the strong positive correlation between Fuel Prices and the Consumer Price Index (CPI)—and its role in defining the store's economic environment.

---

## Exploratory Data Analysis (EDA)
The EDA phase was conducted to validate the following insights:

* **The Economic Squeeze:** Confirmed a linear correlation between Fuel Prices and CPI, indicating that these factors move in tandem to impact consumer purchasing power.
* **Holiday Volatility:** Identified significant "Turbo Spikes" in revenue during specific holiday weeks (Super Bowl, Labor Day, Thanksgiving, and Christmas).
* **Temperature Sensitivity:** Revealed a non-linear (bell-curve) relationship between local temperature and sales, where extreme weather conditions correlate with decreased store traffic.



---

## Technical Implementation

### 1. Data Preprocessing
To prepare the data for machine learning, the following steps were performed:
* **Feature Engineering:** Extracted `Year`, `Month`, and `Week` from the raw `Date` column to capture seasonal patterns.
* **Categorical Encoding:** Applied One-Hot Encoding to the `Store` IDs to treat each of the 45 locations as a distinct entity.
* **Feature Scaling:** Utilized `StandardScaler` to normalize economic variables (Fuel Price, CPI, Unemployment, and Temperature).

### 2. Machine Learning Models
Two high-performance ensemble models were implemented and compared:
* **Random Forest Regressor:** Selected for its stability and ability to handle non-linear patterns and sudden spikes.
* **XGBoost (Extreme Gradient Boosting):** Implemented to optimize the prediction of the "Tandem Duo" relationship by iteratively correcting errors in the economic trend lines.



---

## Evaluation Metrics
The models were evaluated based on the following:
* **R-squared ($R^2$):** Measures the proportion of variance explained by the features.

---

## Requirements
* Python 3.x
* Pandas / NumPy
* Scikit-Learn
* XGBoost
* Matplotlib / Seaborn
