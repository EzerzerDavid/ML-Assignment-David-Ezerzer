# Titanic ML Project

## 📌 Overview
This project applies machine learning techniques to predict passenger survival on the Titanic using logistic regression. The dataset is preprocessed using various feature engineering and transformation techniques, ensuring robust model training and evaluation.

## 📊 Dataset
- **Dataset**: `titanic3.xls`
- **Source**: Kaggle Titanic Dataset
- **Features**: Passenger class, age, fare, number of siblings/spouses, number of parents/children, port of embarkation, etc.
- **Target Variable**: `survived` (1 = survived, 0 = did not survive)

## ⚙️ Preprocessing Steps
1. **Handling Missing Values**:
   - `age` and `fare`: **Median imputation** to prevent outlier influence.
   - `embarked`: **Mode imputation** as it's categorical and missing values are likely missing at random.
2. **Encoding Categorical Variables**:
   - `embarked`: **Target Encoding** to preserve ordinal relationships with survival.
   - `sex`: **OneHotEncoding** since it's a binary categorical variable.
3. **Feature Scaling**:
   - `age` and `fare` standardized using **StandardScaler** (zero mean, unit variance).
   - `age` and `fare` also transformed with **MinMaxScaler** (scaled between 0 and 1) for comparative analysis.
4. **Data Splitting**:
   - **Stratified Train-Validation-Test Split** (70%-15%-15%) to preserve class distribution.
5. **Class Imbalance Handling**:
   - **Logistic Regression with class weighting** (`class_weight='balanced'`) instead of oversampling techniques like SMOTE.

## 🏆 Model Used
- **Logistic Regression** with hyperparameter tuning using **GridSearchCV**.
- **Class weighting applied** to counteract class imbalance.

## 📈 Model Evaluation
### **Validation Performance**
- **Validation Accuracy**: (Update with actual value)
- **Precision, Recall, F1-score** from **Classification Report**.

### **Key Metrics & Visualizations**
1. **Confusion Matrix**:
   - Raw and normalized versions included to assess class-wise performance.
2. **ROC Curve & AUC Score**:
   - Shows trade-off between Sensitivity (True Positive Rate) and Specificity (False Positive Rate).
   - The **optimal decision threshold** is highlighted to maximize model performance.
3. **Cross-Validation Results**:
   - **Mean Cross-Validation Accuracy**: (Update with actual value)
   - Ensures stability across different data splits.

## 📂 Repository Structure
```
📁 Titanic-ML-Project
 ├── MLAssignmentDavidEzerzer.ipynb   # Main notebook
 ├── README.md                   # Project Documentation
 ├── titanic3.xls                # Dataset 
```

## 🚀 Running the Notebook
To run this notebook in Google Colab:
```bash
!git clone https://github.com/EzerzerDavid/Assignment1.git
```

## 🔗 Links
- [Google Colab Notebook] https://colab.research.google.com/drive/1GxqqOeddrDMSsGNguPhAJk_9PibWRR8V?usp=sharing
- [Project Report] 

## 📝 Conclusion
- **Comprehensive Data Preprocessing**: Addressed missing values, categorical encoding, and feature scaling.
- **Robust Model Training & Tuning**: Used **class-weighted Logistic Regression** with hyperparameter tuning.
- **Extensive Model Evaluation**: Implemented **cross-validation, confusion matrix, and ROC analysis** to validate performance.
- **Actionable Insights**: The findings suggest which passenger characteristics were most strongly correlated with survival.

---


