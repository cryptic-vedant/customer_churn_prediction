#  Customer Churn Prediction using Machine Learning

An end-to-end Machine Learning project that predicts customer churn for a subscription-based service using **Decision Tree** and **Support Vector Machine (SVM)**. The project demonstrates the complete ML pipeline, including data preprocessing, exploratory data analysis (EDA), feature selection, model comparison, cross-validation, hyperparameter tuning, and business recommendations.

---

## 📌 Project Overview

Customer churn is one of the most significant challenges for subscription-based businesses. Retaining existing customers is often more cost-effective than acquiring new ones. This project aims to identify customers who are likely to discontinue their subscription, enabling businesses to take proactive retention measures.

The project follows a structured machine learning workflow, from raw data preprocessing to selecting the best-performing model based on multiple evaluation metrics.

---

## 🎯 Objectives

* Perform Exploratory Data Analysis (EDA)
* Clean and preprocess customer data
* Encode categorical variables and scale numerical features
* Apply feature selection techniques
* Train and compare multiple machine learning models
* Perform 5-Fold Cross Validation
* Optimize the best model using GridSearchCV
* Evaluate models using multiple performance metrics
* Provide actionable business recommendations

---

## 📂 Dataset

**Dataset Name:** Telco Customer Churn

**Source:** Kaggle

**Link:** https://www.kaggle.com/datasets/blastchar/telco-customer-churn

### Dataset Summary

* Approximately 7,000 customer records
* 20+ customer-related features
* Binary target variable:

  * Yes → Customer Churned
  * No → Customer Retained

### Features Include

* Customer Demographics
* Contract Information
* Internet Services
* Payment Method
* Monthly Charges
* Total Charges
* Customer Tenure
* Support Services
* Online Security
* Device Usage
* Billing Information

---

## 🛠️ Technologies Used

* Python
* Jupyter Notebook / Google Colab
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib

---

## Project Workflow

```
Dataset
    │
    ▼
Data Cleaning
    │
    ▼
Exploratory Data Analysis (EDA)
    │
    ▼
Feature Encoding
    │
    ▼
Feature Scaling
    │
    ▼
Feature Selection
    │
    ├── Correlation Filtering
    ├── Recursive Feature Elimination (RFE)
    └── Random Forest Feature Importance
    │
    ▼
Model Training
    │
    ├── Decision Tree
    └── Support Vector Machine
    │
    ▼
5-Fold Cross Validation
    │
    ▼
Hyperparameter Tuning
(GridSearchCV)
    │
    ▼
Model Evaluation
    │
    ▼
Business Recommendations
```

---

##  Exploratory Data Analysis (EDA)

The following analyses were performed:

* Dataset overview
* Missing value analysis
* Duplicate value check
* Churn distribution
* Numerical feature distributions
* Categorical feature distributions
* Correlation heatmap
* Feature relationship analysis

---

##  Feature Selection Techniques

Three feature selection methods were implemented:

### 1. Correlation Filtering

Removed highly correlated features to reduce redundancy.

### 2. Recursive Feature Elimination (RFE)

Selected the most informative features using a Decision Tree estimator.

### 3. Random Forest Feature Importance

Ranked features based on their contribution to prediction performance.

---

##  Machine Learning Models

The following classification models were trained and compared:

* Decision Tree Classifier
* Support Vector Machine (SVM)

Both models were evaluated using:

* Full Feature Set
* Reduced Feature Set (RFE)

---

##  Cross Validation

To ensure reliable model performance, **5-Fold Cross Validation** was applied during model comparison.

This reduces dependency on a single train-test split and provides a more robust estimate of model performance.

---

##  Hyperparameter Tuning

The best-performing model was optimized using **GridSearchCV**.

### Parameters Tuned

* C
* Kernel
* Gamma

The tuned model was selected based on cross-validation accuracy.

---

##  Evaluation Metrics

The following evaluation metrics were used:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC Score
* Confusion Matrix
* ROC Curve

---

##  Results

The tuned **Support Vector Machine (SVM)** achieved the best overall performance among all evaluated models.

| Model         | Feature Set      |     Accuracy    |     F1 Score    |     ROC-AUC     |
| ------------- | ---------------- | --------------- | --------------- | --------------- |
| Decision Tree | Full Features    |   0.730305181   |   0.505208333   |   0.662525511   |
| Decision Tree | RFE Features     |   0.737402413   |   0.506666667   |   0.669415381   |
| SVM           | Full Features    |   0.793470546   |   0.551617874   |   0.790906508   |
| SVM           | RFE Features     |   0.784244145   |   0.522012579   |   0.797902297   |
| **Tuned SVM** | **RFE Features** | **0.786373314** | **0.550074738** | **0.808824821** |

---

##  Project Outputs

The repository includes:

* Customer Churn Distribution
* Correlation Heatmap
* Feature Importance Plot
* Model Comparison Charts
* ROC Curve
* Confusion Matrix

---

##  Business Insights

The analysis identified several important factors contributing to customer churn:

* Customers with shorter contract durations are more likely to churn.
* Higher monthly charges increase churn probability.
* Lack of technical support services is associated with increased churn.
* Contract type significantly influences customer retention.
* Long-term customers are less likely to cancel their subscriptions.

---

##  Business Recommendations

### 1. Target High-Risk Customers

Use the trained churn prediction model to identify customers with high churn probability and provide personalized retention offers.

### 2. Improve Customer Support

Enhance customer service quality and provide proactive technical assistance to reduce churn.

### 3. Promote Long-Term Contracts

Offer discounts or incentives for annual subscription plans to increase customer retention.

---

##  Repository Structure

```
Customer-Churn-Prediction/
│
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
│
├── data/
│   └── WA_Fn-UseC_-Telco-Customer-Churn.csv
│
├── notebook/
│   └── Customer_Churn_Prediction.ipynb
│
├── images/
│   ├── churn_distribution.png
│   ├── correlation_heatmap.png
│   ├── feature_importance.png
│   ├── model_accuracy.png
│   ├── roc_curve.png
│   └── confusion_matrix.png
│
├── models/
│   └── best_svm_model.pkl
│
└── results/
    ├── model_comparison.csv
    └── final_model_results.csv
```

---

##  How to Run

1. Clone the repository.

```
git clone https://github.com/yourusername/Customer-Churn-Prediction.git
```

2. Install the required packages.

```
pip install -r requirements.txt
```

3. Open the Jupyter Notebook.

```
jupyter notebook
```

4. Run all cells from top to bottom.

---

##  Future Improvements

* Deploy the model using Streamlit.
* Build a web interface for real-time churn prediction.
* Handle class imbalance using SMOTE.
* Compare with XGBoost and LightGBM.
* Explain predictions using SHAP values.
* Automate retraining with new customer data.

---

## 👨‍💻 Author

**Vedant Tule**

---
