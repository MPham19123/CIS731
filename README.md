# CIS731
Fine-Grained Demand Forecasting Project

Project Overview

This project applies machine learning models to forecast product demand at a granular store-item level using historical sales data. The project compares two models: Facebook’s Prophet (baseline) and XGBoost (comparative). The primary evaluation metrics are MAE, RMSE, and MAPE. The dataset comes from Kaggle’s Store Item Demand Forecasting Challenge.

Data Sources

Original Dataset: Kaggle Store Item Demand Forecasting Challenge

Reference Tutorial: Databricks Fine-Grained Demand Forecasting Solution Accelerator

Data Preparation Steps

Data Import: Loaded 913,000 rows of sales data from Kaggle.

Data Preprocessing:

Executed SQL queries in PySpark to aggregate data by store, item, and date.
Partitioned data by store and item for efficient parallel processing.
Converted to Pandas DataFrame for exploratory analysis.

Feature Engineering:
For XGBoost: Created lag features, rolling averages, and date-based features.
For Prophet: Utilized built-in seasonality detection.

Model Training:
Prophet: Followed Databricks’ prebuilt pipeline.
XGBoost: Trained using custom feature-engineering pipeline.

Evaluation and Testing:
Calculated MAE, RMSE, and MAPE for both models.
Conducted paired t-tests to compare model accuracy.

Forecasting:
Generated 90-day sales forecasts using both models.
Visualized and interpreted results in Pandas and Matplotlib.


Sources

Data Source: Kaggle’s Store Item Demand Forecasting Challenge
https://www.kaggle.com/competitions/demand-forecasting-kernels-only/data

Solution Accelerator: Databricks Fine-Grained Demand Forecasting:
https://notebooks.databricks.com/notebooks/RCG/Fine_Grained_Demand_Forecasting/index.html#Fine_Grained_Demand_Forecasting_1.html

Tutorial References: Kaggle Community Notebooks and ML Resources
https://www.kaggle.com/code/enolac5/time-series-arima-dnn-xgboost-comparison#Model-(2)---Feed-Forward-Neural-Network-with-Daily-Data

