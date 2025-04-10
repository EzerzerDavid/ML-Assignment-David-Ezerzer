## 🚲 Bike Sharing Demand Prediction – ML Assignment 2  
**Author**: David Ezerzer  
**Course**: Machine Learning  
**Notebook**: `assignment_2_<David_Ezerzer[_Ezerzer]>.ipynb`

---

### 📘 Project Overview

This project analyzes and models hourly bike-sharing demand using real-world data. It walks through an end-to-end machine learning pipeline, including exploratory data analysis, feature engineering, model training, tuning, and final evaluation on an unseen test set.

---

### ✅ Tasks Completed

**Task 1 – Exploratory Data Analysis**
- Analyzed distribution of the target variable (`cnt`)
- Identified skewness, outliers, and suspicious temporal patterns
- Visualized effects of weather, time, and binary features

**Task 2 – Data Preprocessing**
- Handled missing values and irrelevant columns
- Investigated potential feature leakage

**Task 3 – Feature Engineering**
- Applied cyclical encoding to time features
- One-hot encoded categorical variables
- Added interaction terms (e.g., `temp * hum`, `hr * workingday`, `temp * season`)
- Scaled continuous features using `StandardScaler`

**Task 4 – Model Training (Linear Regression)**
- Trained a baseline model and evaluated MSE, MAE, RMSE, and R²

**Task 5 – Random Forest**
- Trained and evaluated a default Random Forest model

**Task 6 – Gradient Boosting**
- Introduced Gradient Boosting and performed residual analysis

**Task 7 – Hyperparameter Tuning**
- **Part 1**: Tuned Random Forest with `RandomizedSearchCV`
- **Part 2**: Tuned Gradient Boosting with `BayesSearchCV`
- **Part 3**: Tested XGBoost using tuned parameters

**Task 8 – Iterative Refinement**
- Removed high-end outliers (above 99th percentile) and re-evaluated models

**Task 9 – Final Model Selection**
- Final Gradient Boosting model trained on full training + validation set
- Final test set evaluation performed with strong R² (0.8571)

---

### 📈 Final Model Performance (Test Set)

| Metric         | Value    |
|----------------|----------|
| MSE            | 6929.64  |
| RMSE           | 83.24    |
| MAE            | 55.25    |
| Median AE      | 35.23    |
| MBE            | 36.01    |
| R² Score       | **0.8571** |

---

### 📦 Libraries Used

- Python 3.13  
- pandas, numpy, matplotlib, seaborn  
- scikit-learn  
- xgboost, lightgbm (optional, tested)  
- scikit-optimize (Bayesian optimization)

---

### 💡 Notes

- Feature engineering (especially cyclical and interaction terms) significantly improved model performance.
- Gradient Boosting outperformed all models after tuning and outlier filtering.
- XGBoost provided comparable performance and was included for benchmarking.

---

L
