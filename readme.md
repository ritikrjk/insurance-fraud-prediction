# Insurance Fraud Prediction using Machine Learning

## Overview

This project focuses on predicting fraudulent insurance claims using Machine Learning techniques and exploratory data analysis. The goal was to simulate a real-world insurance fraud detection pipeline by analyzing policyholder information, claim history, and incident-related features to identify suspicious claims.

The project demonstrates practical applications of:

* Data Cleaning
* Feature Engineering
* Exploratory Data Analysis (EDA)
* Statistical Analysis
* Logistic Regression Modeling
* Multicollinearity Detection using VIF

---

# Business Problem

Insurance fraud leads to significant financial losses for insurance companies every year. Detecting fraudulent claims manually is time-consuming and inefficient.

The objective of this project was to:

* Analyze insurance claim data
* Identify patterns associated with fraudulent behavior
* Build a predictive model capable of classifying claims as fraudulent or legitimate

---

# Dataset Information

The dataset contains:

* Policyholder details
* Vehicle information
* Incident reports
* Claim amounts
* Customer demographics
* Insurance policy information

Target Variable:

* `fraud_reported`

  * Y = Fraudulent Claim
  * N = Legitimate Claim

Dataset Size:

* Approximate 1,000 insurance claim records

---

# Project Workflow

## 1. Data Cleaning

Performed extensive preprocessing to improve data quality and prepare the dataset for modeling.

### Tasks Performed

* Handled missing values in columns such as `authorities_contacted`
* Removed unnecessary and duplicate features
* Checked for inconsistencies and invalid values
* Treated categorical and numerical data separately

---

# 2. Exploratory Data Analysis (EDA)

Conducted detailed analysis to understand claim behavior and fraud patterns.

### Analysis Included

* Fraud distribution analysis
* Incident severity trends
* Claim amount comparisons
* Correlation heatmaps
* Categorical feature analysis
* Numerical feature distributions

### Visualization Tools

* Matplotlib
* Seaborn

---

# 3. Feature Engineering

Created new features to improve model performance and capture hidden relationships in the data.

### Feature Engineering Steps

* Converted policy and incident dates into numerical duration-based features
* Extracted:

  * Incident month
  * Incident weekday
  * Policy duration in days
* Encoded categorical variables for machine learning compatibility

These transformations helped improve model interpretability and predictive capability.

---

# 4. Multicollinearity Analysis using VIF

Used Variance Inflation Factor (VIF) analysis to identify highly correlated features.

### Why VIF Was Important

High multicollinearity can:

* Destabilize regression coefficients
* Reduce model interpretability
* Affect prediction reliability

### Actions Taken

* Calculated VIF scores for numerical variables
* Removed highly correlated claim amount features
* Retained only statistically useful variables

This improved model stability and reduced redundancy.

---

# 5. Model Building

Implemented a Logistic Regression model for binary classification.

## Why Logistic Regression?

Logistic Regression was selected because:

* The problem is a binary classification task
* It provides interpretable results
* It performs efficiently on structured tabular datasets

### Steps Performed

* Train-test split
* Feature scaling where required
* Model training
* Prediction generation

---

# 6. Model Evaluation

Evaluated model performance using classification metrics.

### Metrics Used

* Accuracy Score
* Confusion Matrix
* Precision
* Recall
* F1-Score

The model was able to identify fraud-related patterns effectively while demonstrating the importance of feature engineering and preprocessing in predictive analytics.

---

# Key Insights

Some important findings from the analysis:

* Certain incident severities showed stronger fraud association
* Claim-related financial variables had strong correlations
* Feature engineering significantly improved prediction quality
* Data leakage removal was critical to prevent unrealistic model performance

---

# Technologies Used

## Programming Language

* Python

## Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Statsmodels

## Concepts Applied

* Data Cleaning
* EDA
* Feature Engineering
* Logistic Regression
* Multicollinearity Analysis
* Predictive Modeling

---

# Project Structure

```bash
Insurance-Fraud-Prediction/
│
├── data/
├── notebooks/
├── images/
├── README.md
└── requirements.txt
```

# Conclusion

This project focused on building an Insurance Fraud Detection model using Logistic Regression to identify potentially fraudulent insurance claims based on customer, policy, financial, and incident-related features.

During the analysis, multiple preprocessing and feature engineering techniques were applied, including handling categorical variables, removing redundant and high-cardinality features, scaling numerical data using `StandardScaler`, and addressing class imbalance using `class_weight='balanced'`.

Initial model predictions were heavily biased toward the majority class, resulting in poor fraud detection performance. To improve the model, scaling and balanced class weighting were introduced, which significantly improved recall and overall prediction balance.

Final model performance showed:
- Improved fraud detection capability
- Better balance between fraud and non-fraud predictions
- Reduced false positives compared to earlier iterations
- Stronger understanding of classification metrics such as Recall, F1-Score, and Confusion Matrix

This project not only demonstrated the implementation of Logistic Regression for binary classification but also highlighted the importance of feature selection, imbalance handling, preprocessing consistency, and proper model evaluation in real-world machine learning workflows.

Future improvements may include:
- Advanced feature engineering from date-based columns
- Hyperparameter tuning
- Testing ensemble models such as Random Forest or XGBoost
- Applying cross-validation and ROC-AUC analysis for deeper evaluation

Overall, this project served as a practical introduction to fraud analytics, classification modeling, and machine learning problem-solving using Python and Scikit-learn.