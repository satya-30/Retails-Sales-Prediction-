# CS667 Project 2 — Regression Modeling Report

**Date:** 2025-11-05

## Overview
We predict **Total_Amount** per transaction using demographics, product/category, price/discount, channel, payment, region, and calendar features.

## Data Preparation
- Parsed `Date`; engineered `Year`, `Month`, `DayOfWeek`, `IsWeekend`, and `Season`.
- One-hot encoded categorical features (ignore unknowns) and standardized numeric features via `ColumnTransformer`.

## Models & Metrics

| Model                     |       R2 |       MAE |        MSE |      RMSE |
|:--------------------------|---------:|----------:|-----------:|----------:|
| RandomForestRegressor     | 0.999864 |   6.08356 |     96.714 |   9.83433 |
| GradientBoostingRegressor | 0.998397 |  25.9693  |   1141.95  |  33.7928  |
| LinearRegression          | 0.85955  | 232.258   | 100048     | 316.304   |


**Best model by RMSE:** **RandomForestRegressor**

## Visuals
- Actual vs Predicted
- Residuals
- Feature Importances (tree-based)
- Correlation Heatmap

## Insights
- `Quantity` & `Unit_Price` typically drive `Total_Amount`; `Discount` adjusts basket size.
- Temporal and channel features add lift (seasonality/weekend; online/offline effects).
- Category and region capture product mix and regional preferences.

## Next Steps
- Hyperparameter tuning for the best ensemble model.
- Interaction features (e.g., `Quantity * Unit_Price`).
- SHAP values for explainability.
