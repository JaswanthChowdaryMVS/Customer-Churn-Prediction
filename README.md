# Customer Churn Prediction & Retention Recommendation System

## 📌 Project Overview

Customer churn is a major business challenge because losing existing customers can directly impact revenue and customer lifetime value.

This project develops an end-to-end machine learning system that predicts the probability of customer churn, identifies high-risk customers, explains model predictions using SHAP, and provides actionable retention recommendations.

## 🎯 Business Problem

The objective is to identify customers who are likely to churn and provide a risk-based approach that can help businesses prioritize customer retention efforts.

The project answers questions such as:

- Which customers are most likely to churn?
- What factors are driving customer churn?
- How can high-risk customers be identified?
- How can machine learning predictions be converted into actionable retention strategies?

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- SHAP
- Joblib
- Jupyter Notebook

## 🔍 Project Workflow

1. Business understanding
2. Data loading and quality checks
3. Data cleaning and preprocessing
4. Exploratory Data Analysis (EDA)
5. Train / validation / test split
6. Feature preprocessing
7. Baseline modeling
8. Logistic Regression
9. Random Forest
10. XGBoost
11. Cross-validated hyperparameter tuning
12. Model evaluation
13. Classification threshold optimization
14. SHAP-based explainability
15. Customer risk segmentation
16. Retention recommendations
17. New-customer prediction
18. CSV prediction export

## 🤖 Machine Learning Models

The project evaluates multiple models:

- Dummy Classifier baseline
- Logistic Regression
- Random Forest
- XGBoost

XGBoost is tuned using cross-validated hyperparameter search.

## 📊 Model Evaluation

The models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- PR-AUC
- Confusion Matrix
- ROC Curve
- Precision-Recall Curve

Because churn is a business-risk problem, the project also evaluates different classification thresholds instead of relying only on the default 0.50 threshold.

## 🎯 Threshold Optimization

The classification threshold is optimized using the validation set by searching thresholds from 0.10 to 0.90.

The threshold that provides the best validation F1-score is selected, with the lower threshold used as the tie-breaker.

The test set remains untouched until final evaluation.

## 🔎 Explainable AI

SHAP (SHapley Additive exPlanations) is used to understand why the model makes its predictions.

The project includes:

- Global feature importance
- Local customer-level explanations

This helps translate machine learning predictions into understandable business insights.

## 👥 Customer Risk Segmentation

Customers are assigned risk levels based on their predicted churn probability:

- High Risk
- Medium Risk
- Low Risk

Retention recommendations are generated based on customer characteristics and risk level.

## 🚀 New Customer Prediction

The final model can be used to score new customer records.

The prediction workflow:

1. Loads the saved model artifact
2. Validates input columns
3. Applies the same preprocessing pipeline
4. Generates churn probability
5. Applies the optimized classification threshold
6. Assigns a customer risk level
7. Generates a retention recommendation
8. Exports predictions to CSV

## 📁 Project Structure

```text
Customer-Churn-Prediction/
│
├── Customer_Churn_Prediction.ipynb
├── README.md
├── requirements.txt
├── data/
│   └── README.md
├── models/
│   └── customer_churn_model_artifact.joblib
└── predictions/
    └── README.md
