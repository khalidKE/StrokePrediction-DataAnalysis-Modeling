# 🧠 Brain Stroke Prediction

This project aims to predict the likelihood of a brain stroke occurrence using machine learning techniques. Leveraging a real-world dataset from Kaggle, we explore multiple models to evaluate prediction accuracy and performance.

## 📂 Dataset

The dataset used is publicly available on Kaggle:

🔗 **[Kaggle Notebook Link](https://www.kaggle.com/code/reihanenamdari/brain-stroke-prediction-decisiontree/notebook)**
🔢 **Size**: 4,981 rows × 11 columns
🎯 **Target Variable**: `stroke` (binary: `0 = no`, `1 = yes`)
🧾 **Key Features**:

* `gender`
* `age`
* `hypertension`
* `heart_disease`
* `ever_married`
* `work_type`
* `Residence_type`
* `avg_glucose_level`
* `bmi`
* `smoking_status`

📊 **Data Types**: Mixture of numerical and categorical features

## 🔍 Data Inspection

* **First & Last Rows**: Used to verify data consistency.
* **Missing Values**: No missing data detected in any column.
* **Summary Statistics**:

  * Age: Mean = 43.4 years (Range: 0.08 to 82)
  * Hypertension prevalence: \~9.6%
  * Heart Disease prevalence: \~5.5%
  * Avg Glucose Level: 105.9
  * Avg BMI: 28.5
  * Positive Stroke Cases: 248 out of 4,981

## 🛠️ Data Preparation

* **Feature/Target Split**: Separated `stroke` as the target variable.
* **Encoding**: Label encoding for categorical variables (`gender`, `work_type`, etc.).
* **Split**: 70% training data, 30% testing data.

## 🤖 Machine Learning Models

### 1. Logistic Regression

* Max Iterations: 1000
* Training Accuracy: **94.98%**
* Test Accuracy: **95.12%**

### 2. Decision Tree Classifier

* Training Accuracy: **100%** *(possible overfitting)*
* Test Accuracy: **90.77%**
* Note: Simple, interpretable model

### 3. Gradient Boosting Classifier

* Training Accuracy: **95.61%**
* Test Accuracy: **94.72%**
* Parameters:

  * Estimators: 100
  * Learning Rate: 0.1
  * Max Depth: 3

### 4. Random Forest Classifier

* Training Accuracy: **97.13%**
* Test Accuracy: **95.05%**
* Parameters:

  * Trees: 100
  * Max Depth: 10

## ✅ Summary

* **Data Quality**: Clean and complete, no missing values.
* **Model Performance**: High test accuracy for all models.
* **Best Model**: **Random Forest Classifier** (balanced performance with minimal overfitting)

## 🚀 Future Work

* Advanced feature engineering
* Hyperparameter optimization
* Model deployment for real-time predictions
