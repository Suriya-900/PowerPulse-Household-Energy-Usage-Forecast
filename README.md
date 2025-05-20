# PowerPulse-Household-Energy-Usage-Forecast

# ⚡ Energy Consumption Forecasting using Machine Learning

This project aims to predict **Global Active Power Consumption** using historical energy usage data and various machine learning regression models. The dataset is based on real-time measurements of power and sub-metering collected from a household.

## 📌 Project Highlights

- Time-based feature engineering (hour, day, weekday, peak hours)
- Rolling statistics: rolling mean (15 min, 1 hour), daily average
- Multiple regression models: Linear Regression, Random Forest, XGBoost
- Hyperparameter tuning (GridSearchCV) on Random Forest
- Performance comparison via metrics and visualizations
- Residual analysis to evaluate model fit

---

## 🧠 Machine Learning Models

| Model                  | RMSE     | MAE      | R² Score |
|------------------------|----------|----------|----------|
| Linear Regression      | 0.0401   | 0.0255   | 0.9986   |
| Random Forest          | 0.0242   | 0.0109   | 0.9995   |
| XGBoost                | 0.0284   | 0.0168   | 0.9993   |
| Tuned Random Forest    | 0.0299   | 0.0139   | 0.9992   |

---

## 📊 Visualizations

- **Actual vs Predicted Scatter Plot**: Shows how close predicted values are to true values.
- **Time Series Comparison**: Plots of actual vs predicted power consumption.
- **Correlation Heatmap**: Relationships between features and target variable.

---
## Correlation Heatmap
High correlation between Global_active_power and:

Sub_metering_3 (0.64)

Global_intensity (0.63)

Sub_metering_1, Sub_metering_2

Voltage shows weak or negative correlations, indicating it's less impactful on its own.

## 🛠️ Features Used

- Temporal features: `hour`, `day`, `month`, `weekday`, `is_peak_hour`
- Electrical measurements: `Voltage`, `Global_reactive_power`, `Global_intensity`
- Sub-metering: `Sub_metering_1`, `Sub_metering_2`, `Sub_metering_3`
- Rolling statistics: `rolling_mean`, `rolling_mean_1hr`, `daily_avg_power`

---

## 📁 Dataset Structure

Sample format:

| datetime            | Global_active_power | Global_reactive_power | Voltage | Global_intensity | Sub_metering_1 | Sub_metering_2 | Sub_metering_3 |
|---------------------|---------------------|------------------------|---------|------------------|----------------|----------------|----------------|
| 2006-12-16 17:24:00 | 4.216               | 0.418                  | 234.84  | 18.4             | 0.0            | 1.0            | 17.0           |

---

##🌿 How This Helps Households Save Energy


1. Personalized Energy Planning:

Predict usage trends and optimize appliance use timing.

2. Anomaly Detection:

Spot sudden spikes indicating broken or inefficient appliances.

3. Smart Home Integration:

Automate actions like turning off high-consumption devices during peak hours.

4. Environmental Impact:

Reduced energy waste = Lower carbon emissions


✅ Interpretation:
Random Forest is the best overall (lowest RMSE & MAE, highest R²).

XGBoost is close behind.

Linear Regression performs well but less precise than ensemble methods.



