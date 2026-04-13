# credit-risk-ml-prediction
Predicting loan defaults using machine learning to enable smarter and safer lending decisions.

Overview

Credit risk assessment is a critical problem in the financial industry. Traditional rule-based systems struggle to adapt to changing borrower behavior, especially after events like COVID-19.

This project builds a machine learning-based credit risk prediction system that helps:
->Identify high-risk borrowers
->Reduce non-performing loans (NPLs)
->Support data-driven lending decisions

Problem Statement

Financial institutions face:
->Increasing loan defaults
->Imbalanced datasets (very few defaulters vs many non-defaulters)
->Complex borrower behavior not captured by traditional models

Goal: Build a model that can accurately predict credit risk while handling real-world challenges like imbalance and noisy data.

Dataset & Features

The dataset includes:
-> Customer demographics (age, marital status, education)
-? Financial data (income, loan history)
-> Credit behavior (delinquency, past loans)

Data Preprocessing Pipeline

A strong preprocessing pipeline was built to ensure high-quality input data:

-> Data Cleaning
Removed invalid values (-99999)
Dropped highly noisy columns
Merged datasets using PROSPECTID

-> Feature Selection
Chi-Square Test → categorical features
VIF (Variance Inflation Factor) → removed multicollinearity
ANOVA → validated numerical features

-> Encoding
Ordinal encoding (Education)
One-hot encoding (categorical variables)

-> Outlier Handling
IQR-based filtering

Models Used and Training

We experimented with multiple machine learning models:
-> Decision Tree	(Simple and interpretable)
-> Random Forest	(Ensemble method reducing overfitting)
-> XGBoost	(High-performance gradient boosting)

* Used 5-fold cross-validation
* Evaluated using: Accuracy , Precision , Recall , F1-score
* Hyperparameter Tuning: Performed Grid Search

Results

Best Model: XGBoost
-> Accuracy: 78%
-> Strong recall for majority class (P2)
-> Balanced performance across key categories

Key Insights
-> Tree-based models handled data well
-> Feature scaling was not required
-> Class imbalance remained a challenge

Industry Relevance

This project aligns with real-world applications like:
-> Credit scoring systems
-> Risk management platforms
-> Fraud detection systems
