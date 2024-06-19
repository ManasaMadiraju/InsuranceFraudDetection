# InsuranceFraudDetection

## Overview
The insurance industry is vast and complex, offering diverse policies like car, rental, health, and life insurance. Unfortunately, insurance fraud is widespread, occurring throughout the process from policy sales to claims. To combat this, insurance companies need sophisticated tools, including data analytics and machine learning, to detect and deter fraudulent activities. Fraud can be perpetrated by individuals, groups, policyholders, insurers, or third parties. Due to its scope and complexity, robust solutions are essential. Insurance fraud costs both insurers and policyholders billions annually and can take various forms such as false claims, fake policies, and identity theft.

This project aims to develop a machine learning model that analyzes historical claims and policyholder data to detect insurance fraud. Our goal is to uncover patterns and trends that signal fraudulent behavior.

## Dataset
We utilize an insurance dataset with 1,000 rows of claims, each including 40 features such as "age," "claim amount," "authorities reported," etc., and a label indicating whether fraud occurred.

## Data Preparation
1. **Handling Missing Values:** Missing values are addressed by either dropping columns or creating new categories.
2. **Feature Engineering:**
   - Identify redundant features using a correlation matrix.
   - Consolidate dominant categories.
   - Check for class imbalance to detect bias.
3. **Encoding:**
   - Categorical variables are encoded using One Hot Encoding.
   - Classes are encoded with Label Binarizer.

## Models
We employ two machine learning models to detect insurance fraud:
1. **Random Forest Classifier**
2. **XGBoost**

## Model Evaluation
The models are evaluated using various performance metrics. The dataset is divided into 80% for training-validation and 20% for testing.

### Random Forest Classifier
- **Hyperparameter Tuning:** Grid Search is used for hyperparameter tuning. GridSearchCV generates candidates from a grid of parameter values.

### XGBoost
- **Hyperparameter Tuning:** Bayesian Optimization is used for hyperparameter tuning. This method tracks past evaluations to create a probabilistic model mapping hyperparameters to their likelihood of achieving a high score. The objective function is validated across three sets, producing a mean score.
