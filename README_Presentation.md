# 🗣️ Retail Sales Prediction — Presentation Script

**Good morning, Professor Sarbanes,**

My name is *Venkata Satya Sai Sreshta Penumatcha*, and I’ll be presenting my project — **Retail Sales Prediction using Machine Learning.**

---

## 🎯 Introduction
For this project, I worked with a synthetic retail dataset containing **50,000 transactions**.  
Each record represents a customer purchase with features like *Transaction ID, Date, Gender, Age, Quantity, Unit Price, Discount,* and the final *Total Amount*.  
The main goal was to predict the **Total Sales Amount** and understand which factors drive sales performance.

---

## 📊 Exploring the Data
Before modeling, I performed **Exploratory Data Analysis (EDA)** to understand the structure and relationships in the data.

- The **Total Amount** column was right-skewed — most transactions were small to medium, with a few high-value outliers.  
- **Gender** distribution was fairly balanced, showing equal participation across demographics.  
- **Age** was centered between 20 and 40 years, indicating a young to mid-aged customer base.  
- A **correlation heatmap** confirmed that *Quantity* and *Unit Price* were the strongest predictors of Total Amount.

These observations provided the foundation for my feature selection and modeling approach.

---

## ⚙️ Feature Engineering
- Derived new features like **Day of the Week** and **IsWeekend** from transaction dates to capture temporal trends.  
- Encoded **Gender** numerically using Label Encoding.  
- Applied **StandardScaler** to normalize numerical features for better model performance.  

---

## 🤖 Model Building and Evaluation
I compared three machine learning regression models:

| Model | R² | MAE | MSE | RMSE |
|--------|----|-----|------|------|
| **Random Forest Regressor** | **0.999864** | **6.08** | **96.71** | **9.83** |
| Gradient Boosting Regressor | 0.998397 | 25.97 | 1141.95 | 33.79 |
| Linear Regression | 0.859550 | 232.26 | 100048.03 | 316.30 |

✅ **Best Model:** *Random Forest Regressor* — R² of 0.9999, showing almost perfect accuracy and minimal error.

---

## 📈 Model Interpretation
- **Actual vs Predicted Plot:** Points aligned closely to the diagonal, confirming strong predictive performance.  
- **Residual Plot:** Residuals were evenly spread around zero, showing no bias in predictions.  
- **Feature Importance:** Top predictors were *Unit Price*, *Quantity*, and *Discount*, which aligns with business logic.  

---

## 💡 Business Insights
1. **Unit Price** and **Quantity** directly impact revenue — strategic pricing and bundling can increase sales.  
2. **Discounts** negatively affect total revenue — suggesting the need for controlled discounting.  
3. **Weekend transactions** are slightly higher, indicating that weekend promotions could boost overall performance.

---

## 🧠 Conclusion
This project demonstrates how **machine learning** can be used to analyze and predict retail sales effectively.  
The Random Forest model provided **high accuracy and interpretability**, making it suitable for real-world business forecasting.  
The insights gained can guide **pricing strategy, marketing timing, and inventory decisions** in a retail environment.

---

**Thank you, Professor,** for reviewing my project.  
I’d be happy to discuss the data, models, or insights in more detail.
