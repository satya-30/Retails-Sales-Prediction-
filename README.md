# 🛒 Retail Sales Prediction using Machine Learning

## 📘 Project Overview

This project predicts **Total Sales (Revenue)** from retail transaction data using **machine learning regression models**.
It demonstrates a full data science workflow — from **EDA and feature engineering** to **model evaluation and interpretation**.

---

## 🎯 Objectives

* Explore and clean the dataset through EDA.
* Build regression models to predict total revenue.
* Compare models using R², MAE, MSE, and RMSE.
* Identify key features influencing sales outcomes.

---

## 📊 Dataset Description

* **File:** `retail_data_synthetic_50k.xlsx`
* **Records:** 50,000 transactions
* **Columns:**
  `Transaction_ID`, `Date`, `Customer_ID`, `Gender`, `Age`, `Quantity`, `Unit_Price`, `Discount`, `Total_Amount`

---

## 🔍 Exploratory Data Analysis (EDA)

EDA revealed core sales trends and patterns:

* **Total Amount**: Right-skewed — most transactions are low to mid value.
* **Gender**: Balanced distribution of male and female customers.
* **Quantity & Unit Price**: Positively correlated with Total Sales.
* **Heatmap**: Strong correlation between Quantity, Unit Price, and Total Amount.

Visuals included:

* Histograms for Total_Amount, Quantity, and Unit_Price
* Scatterplot of Quantity vs. Total_Amount
* Correlation Heatmap
* Gender-based count plots

---

## ⚙️ Feature Engineering

* Extracted **DayOfWeek** and **IsWeekend** features from transaction dates.
* Encoded **Gender** numerically using LabelEncoder.
* Applied **StandardScaler** to normalize numerical columns.

---

## 🤖 Machine Learning Models

The following regression models were trained and compared:

| Model                           | R²           | MAE      | MSE       | RMSE     |
| ------------------------------- | ------------ | -------- | --------- | -------- |
| **Random Forest Regressor**     | **0.999864** | **6.08** | **96.71** | **9.83** |
| **Gradient Boosting Regressor** | 0.998397     | 25.97    | 1141.95   | 33.79    |
| **Linear Regression**           | 0.859550     | 232.26   | 100048.03 | 316.30   |

📊 **Best Model:** Random Forest Regressor

* Achieved near-perfect R² (0.9999)
* Extremely low prediction error (MAE ≈ 6.08)

---

## 📈 Model Evaluation & Visualization

Visualizations created:

* **Actual vs Predicted Plot** — shows close alignment between true and predicted sales.
* **Residual Plot** — random distribution of residuals → unbiased predictions.
* **Feature Importance Plot** — top predictors: *Unit Price*, *Quantity*, and *Discount*.
* **Correlation Heatmap** — validates relationships across numerical features.

---

## 💡 Business Insights

* **Price per Unit** and **Quantity** are key revenue drivers.
* Higher **discounts** reduce total revenue.
* Weekends show slightly higher purchase volumes.
* The model can support **inventory optimization, pricing strategy,** and **sales forecasting**.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn, xgboost
* **Environment:** Jupyter Notebook / Google Colab

---

## 🚀 How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/<your-username>/Retail-Sales-Prediction-ML.git
   cd Retail-Sales-Prediction-ML
   ```
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Open and run the notebook:

   ```bash
   jupyter notebook Project_2_Colab.ipynb
   ```

---

## 🧾 Author

**Venkata Satya Sai Sreshta Penumatcha**
🎓 *MS in Data Science, Pace University*
📧 vp20967n@pace.edu
💼 Interests: Data Science • Machine Learning • Business Analytics

---

## 📚 Acknowledgment

Course: **CS667 – Practical Data Science**
Instructor: **Prof. Sarbanes**
Institution: **Pace University (Fall 2025)**
