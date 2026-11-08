# 🏠 House Prices - Advanced Regression Techniques

A Machine Learning project focused on predicting residential house prices using regression techniques and feature engineering.

This project is part of my Machine Learning learning journey, where I explore data preprocessing, exploratory data analysis, feature engineering, model evaluation, and ensemble methods.

## 📌 Competition

**Kaggle:** [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)

**Problem Type:** Supervised Learning – Regression

**Objective:** Predict the final sale price of residential homes in Ames, Iowa, based on various property features.

## 🛠️ Tech Stack

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- LightGBM
- SciPy

## 🔍 Workflow

### 1. Exploratory Data Analysis (EDA)

- Analyzed dataset structure and distributions.
- Investigated missing values.
- Examined correlations between numerical features and SalePrice.
- Visualized relationships between house features and sale prices.
- Identified potential outliers.

### 2. Data Cleaning & Preprocessing

- Removed selected outliers based on GrLivArea and SalePrice.
- Applied log transformation to the target variable.
- Handled missing values based on feature meanings.
- Used median and mode imputation where appropriate.
- Applied ordinal encoding to quality-related categorical features.
- Used one-hot encoding for categorical variables.

### 3. Feature Engineering

Created additional features to capture more meaningful information about properties:

- `TotalBath`: Total number of bathrooms.
- `TotalSF`: Combined living area.
- `TotalPorchSF`: Total porch and deck area.
- `QualSF`: Overall quality multiplied by total area.
- `HouseAge`: Relative house age.
- `RemodAge`: Relative remodeling age.
- Binary features indicating the presence of a garage, basement, pool, fireplace, and second floor.

Also applied log transformations to highly skewed numerical features.

### 4. Model Training & Evaluation

Compared multiple regression algorithms using 5-Fold Cross-Validation.

| Model | Approach |
|---|---|
| Lasso Regression | Regularized Linear Regression |
| ElasticNet | L1 + L2 Regularization |
| Ridge Regression | L2 Regularization |
| Gradient Boosting | Boosting Ensemble |
| XGBoost | Gradient Boosting Framework |
| LightGBM | Gradient Boosting Framework |

**Evaluation Metric:** Root Mean Squared Error (RMSE) on the log-transformed target.

### 5. Model Ensembling

Experimented with out-of-fold predictions and model blending.

The final submission combines predictions from:

- Lasso Regression
- Gradient Boosting Regressor

Using an equal-weight average of their predictions.

Predictions are transformed back to the original price scale using `expm1()`.

## 📊 Results

- Validation strategy: 5-Fold Cross-Validation.
- Model comparison: 6 regression models.
- Final approach: Lasso + Gradient Boosting blending.
- Kaggle submission: Generated successfully.

*Kaggle leaderboard score: To be updated.*


