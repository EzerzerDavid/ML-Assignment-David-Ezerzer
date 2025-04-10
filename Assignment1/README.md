---

## **Titanic Survival Prediction - Machine Learning Assignment**
### **Author:** David Ezerzer  
This project applies machine learning techniques to predict survival outcomes on the Titanic dataset. The workflow includes Exploratory Data Analysis (EDA), feature engineering, categorical encoding, class balancing, and model evaluation.

---

## **📂 Project Structure**
```
📁 Titanic-Survival-Prediction
│-- 📄 MLAssignmentDavidEzerzer.ipynb    # Main Jupyter Notebook
│-- 📄 README.md                          # Project Documentation (this file)
│   ├── titanic3.xls                      # Titanic dataset (must be uploaded manually)
```

---

## **📊 Workflow & Methodology**
### **1️⃣ Exploratory Data Analysis (EDA)**
- Visualized the dataset structure, missing values, and feature distributions.
- Identified relationships between independent variables and survival outcome.
- Heatmap and count plots used to understand class distribution.

### **2️⃣ Data Preprocessing**
- **Handling Missing Values**:
  - **Numerical Features**: Median imputation (e.g., 'age', 'fare') to handle skewness.
  - **Categorical Features**: Mode imputation (e.g., 'embarked') to preserve consistency.
- **Feature Selection**: Removed non-informative columns like passenger names, ticket numbers, and cabin IDs.

### **3️⃣ Encoding Categorical Variables**
- **One-Hot Encoding for 'sex'** (Binary variable, treated as independent categories).
- **Target Encoding for 'embarked'** (Applied **only after data splitting** to prevent data leakage).

### **4️⃣ Feature Scaling**
- **Standardization (StandardScaler)** for normally distributed features (e.g., 'age', 'fare').
- **MinMax Scaling** as an alternative approach for features with non-normal distributions.

### **5️⃣ Splitting the Dataset**
- **Training (60%)**, **Validation (20%)**, and **Test (20%)** to ensure fair model evaluation.
- Stratified split used to maintain class balance.

### **6️⃣ Handling Class Imbalance**
- Applied **Synthetic Minority Oversampling Technique (SMOTE)** to balance classes.
- Ensured minority class predictions were not penalized.

### **7️⃣ Model Training & Evaluation**
- **Logistic Regression** used for classification.
- Evaluated using:
  - **Accuracy, Precision, Recall, F1-score** for classification performance.
  - **Confusion Matrix & Normalized Confusion Matrix** for error analysis.
  - **ROC Curve & AUC Score** for model discrimination power.
- **Cross-validation** to ensure model generalizability.

---

## **🚀 How to Run the Notebook**
### **Option 1: Run in Google Colab (Recommended)**
1. Upload `titanic3.xls` to your Google Drive.
2. Mount Google Drive in the notebook:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```
3. Update the file path:
   ```python
   file_path = "/content/drive/My Drive/titanic3.xls"
   df = pd.read_excel(file_path)
   ```
4. Run all cells.

### **Option 2: Run Locally**
1. Install required libraries:
   ```bash
   pip install pandas numpy seaborn scikit-learn category_encoders imbalanced-learn matplotlib
   ```
2. Place `titanic3.xls` in the project directory.
3. Run the notebook using Jupyter Notebook or Jupyter Lab.

---

## **📈 Results & Observations**
- **Best Model Accuracy (Validation Set):** **~82.6%**
- **AUC Score:** **High (~0.85), indicating strong classifier performance.**
- **Key Features Impacting Survival:**  
  - **Gender:** Females had a higher survival rate.
  - **Passenger Class:** Higher-class passengers had better survival chances.
  - **Embarkation Port:** Some ports had a higher correlation with survival.
  
---
