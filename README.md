# Fraud-Detection
**About the Project**

Credit card fraud is rare, but extremely impactful. In this project, I built a machine learning model to detect fraudulent transactions early. Since fraud cases are very rare (less than 0.2%), the project required careful handling of imbalanced data and performance metrics beyond accuracy.

**Dataset Info**
Source: Kaggle – Credit Card Fraud Detection

Total transactions: 284,807

Fraud cases: 492

**Features:**

V1 to V28: Anonymized PCA components

Amount: Transaction amount

Time: Seconds since the first transaction

Class: 0 for normal, 1 for fraud

**Step-by-Step Process**
1. Exploratory Data Analysis (EDA)
Performed data exploration to understand the distribution of fraud vs non-fraud cases, transaction amounts, and correlation between features.

2. Data Preprocessing
Checked for missing values

Standardized Amount and Time using StandardScaler

3. Handling Imbalanced Data
Used SMOTE (Synthetic Minority Oversampling Technique) to oversample the minority class (fraud). This helped the models learn fraud patterns more effectively without biasing toward the majority class.

**Model Comparison**


![image](https://github.com/user-attachments/assets/d31a54e6-a431-4ade-829b-2c9829f2f4b6)

**Insight:**
Random Forest had high recall but very low precision, meaning it predicted a lot of false frauds.

Logistic Regression was more balanced but missed many frauds (low recall).

XGBoost performed the best overall, especially after tuning—achieving both good precision and high recall.

**Final Model Performance**

Final tuned XGBoost model:

Accuracy: 100% (because of class imbalance)

Precision (fraud): 0.79

Recall (fraud): 0.86

F1-score (fraud): 0.82

**Output Files**

fraud_detection_xgboost_model.pkl: Trained model

test_data_for_demo.csv: Sample test data

