# Construction Cost Estimation & Pricing Analysis

This project builds a data-driven pipeline to analyze construction cost components and predict total project estimates using machine learning. It combines exploratory data analysis (EDA), feature engineering, and a regression model to understand pricing strategies and estimate costs accurately.

---
## Project Overview

The goal of this project is to:

* Analyze how different cost components impact total construction estimates
* Understand the role of pricing policies (e.g., discounts, markups)
* Build a predictive model for **Total_Estimate**
* Interpret model coefficients for business insights
---
## Dataset
The dataset (`construction_estimates.csv`) includes:
* **Material_Cost** – Cost of materials
* **Labor_Cost** – Labor expenses
* **Profit_Rate** – Profit margin percentage
* **Discount_or_Markup** – Adjustments applied to pricing
* **Policy_Reason** – Business reason for pricing decisions
* **Total_Estimate** – Final project estimate (target variable)
---
## Exploratory Data Analysis
The project includes:
* Distribution and relationship analysis using pairplots
* Correlation heatmap to identify key relationships
* Policy-based breakdowns of:
  * Profit rate
  * Discounts/markups
Example insights:
* Strong linear relationship between costs and total estimate
* Policy decisions influence pricing adjustments significantly
---
## Model Pipeline
A machine learning pipeline is built using **scikit-learn**:
### Preprocessing:
* Standardization of numerical features
* One-hot encoding of categorical variables
### Model:
* Linear Regression
### Pipeline:
```python
Pipeline([
    ('preprocessor', ColumnTransformer(...)),
    ('regressor', LinearRegression())
])
```
---
## Model Performance
* **Train R²:** 0.9971
* **Test R²:**  0.9970
The model shows excellent predictive performance, indicating strong linear relationships in the data.
---
## Feature Importance & Interpretation
Key drivers of total estimate:
* **Material_Cost & Labor_Cost** → strongest contributors
* **Profit_Rate** → significant impact on final price
* **Discount_or_Markup** → nearly 1-to-1 effect
* **Policy_Reason** → measurable influence depending on category
---
## Technologies Used
* Python
* Pandas & NumPy
* Matplotlib & Seaborn
* Scikit-learn



