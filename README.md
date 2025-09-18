# Chicago Crimes Analysis and Forecasting (2020–2022)
## 📌 Project Overview

This project analyzes and forecasts crime trends in Chicago using Python (for time series modeling) and Tableau (for interactive visualizations). The analysis focuses on patterns across years 2020, 2021, and 2022, exploring trends by district, time of day, months, and holidays, while also detecting cycles and seasonality in crime data.

A special emphasis is placed on time series forecasting for specific crime types: Theft and Narcotics.

## 🛠️ Tools & Technologies

### Python

Pandas & NumPy (data cleaning and preprocessing)

Matplotlib & Seaborn (visualization)

Statsmodels (manual ARIMA/SARIMA modeling)

Pmdarima (auto_arima tuning and diagnostics)

### Tableau

Interactive dashboards

District-level and time-based crime analysis

Dataset: Chicago crime records (2020–2022)

## 🔍 Analysis Topics

Police Districts – Which district had the most vs. least crimes in 2022?

Yearly Trends – Is crime overall increasing or decreasing? Which crimes show opposite trends?

Rush Hours (AM vs. PM) – Comparing 7–10 AM vs. 4–7 PM. What are the top 5 crimes in each? Are motor vehicle thefts more common in AM or PM?

Monthly Trends – Which months are high/low crime? Which crimes break the pattern?

Holiday Crimes – Top 3 holidays with the most crimes + top 5 crimes for each holiday.

Seasonality – Detecting cycles and recurring crime patterns.

Forecasting Theft vs. Narcotics – Building and evaluating time series models.

## 📊 Forecasting Methodology

For Theft and Narcotics, the following steps were applied:

Data Transformation

Converted crime data into a monthly time series using .size().

Checked for and handled null values.

Time Series Exploration

Decomposed the series to detect seasonality.

Applied non-seasonal and/or seasonal differencing if needed.

Used ACF and PACF plots to guide ARIMA/SARIMA order selection.

Modeling

Split data into training and test sets (6-month forecast horizon).

Fit a manual ARIMA/SARIMA model based on exploratory analysis.

Generated forecasts and compared predictions vs. test data.

Evaluated models using metrics (MAE, RMSE, MAPE).

Auto ARIMA Tuning

Applied pmdarima.auto_arima to find best parameters.

Fit model on training data with optimal parameters.

Re-evaluated metrics and forecast accuracy.

Final Model Selection

Compared manual vs. auto_arima results.

Justified the final model choice using metrics and diagnostics.

True Forecasting

Trained the final model on the entire dataset.

Produced forecasts beyond 2022 for Theft and Narcotics.

## 📈 Forecast Evaluation

For each crime type:

Calculated predicted net change (raw counts) from start to end of forecast.

Converted raw delta into percent change.

## Final Comparative Questions

Which of the two crimes is forecasted to have the highest monthly count by the end?

Which shows the largest net change?

Which shows the largest percent change?

## Final Recommendations

Summarized insights for stakeholders.

Provided reporting-quality visuals (time series + forecasts).

Suggested focus areas for law enforcement resource allocation.
