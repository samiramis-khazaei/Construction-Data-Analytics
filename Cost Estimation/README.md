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

<img width="1231" height="1231" alt="image" src="https://github.com/user-attachments/assets/81f78cfd-709b-4967-8a8e-4604e53bae7d" />
 
* Correlation heatmap to identify key relationships

<img width="633" height="792" alt="image" src="https://github.com/user-attachments/assets/0f4a6237-74a0-4ef5-a8bc-de18beba91a2" />

 
* Policy-based breakdowns of:
  * Profit rate
    
 <img width="1218" height="540" alt="image" src="https://github.com/user-attachments/assets/bfbfa20a-97a5-4e6a-8a09-444c2df36fcf" />
 
  * Discounts/markups
    
 <img width="1256" height="493" alt="image" src="https://github.com/user-attachments/assets/7172797f-f222-40f3-a6bd-22a27e5c6a2c" />

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

<img width="1298" height="562" alt="image" src="https://github.com/user-attachments/assets/3c282955-67c2-4580-b731-b8d55bd7e686" />
  
---
## Technologies Used
* Python
* Pandas & NumPy
* Matplotlib & Seaborn
* Scikit-learn



