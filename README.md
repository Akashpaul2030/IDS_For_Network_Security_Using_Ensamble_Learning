# # Intrusion Detection System (IDS) Analysis

## Project Overview

This project focuses on developing and evaluating machine learning models for an Intrusion Detection System (IDS) using the KDD Cup 1999 dataset. The primary objective is to accurately classify network traffic as either normal or an attack. In ensamble learning (Random_forest & Gradient boosting) using I got 99.86% high accuracy.

## Dataset

- **Source**: [KDD Cup 1999 dataset](https://kdd.org/kdd2023/call-for-kdd-cup-proposals/index.html)
- **Features**: 41 features including duration, protocol type, service, flag, src_bytes, dst_bytes, etc.
- **Target Variable**: Binary classification (normal vs. attack)

## Methodology

### 1. Data Preprocessing
- Loaded and inspected the dataset
- Handled missing values (none found)
- Encoded categorical variables

### 2. Feature Selection
- Applied mutual information and chi-square tests to select the most important features
- Selected top 15 features for model training

### 3. Model Development
The following models were developed and evaluated:

- Logistic Regression
- XGBoost
- Random Forest
- Support Vector Machine (SVM)
- Ensemble models (various combinations of the above)

### 4. Model Evaluation

Models were evaluated based on the following metrics:

- Confusion Matrix
- Classification Report (Precision, Recall, F1-Score)
- ROC-AUC Score
- Precision-Recall Curve

## Key Findings

1. **Feature Importance**: The most important features for detecting intrusions include:
   - `src_bytes`
   - `dst_bytes`
   - `duration`
   - `dst_host_srv_count`
   - `count`

2. **Model Performance**: 
   - All models performed well with high accuracy and F1-scores
   - Ensemble models (especially Random Forest + XGBoost) showed the best overall performance

3. **ROC-AUC Scores**: The ensemble models achieved ROC-AUC scores close to 1, indicating excellent discriminative ability.

## Future Work

1. Experiment with more advanced feature engineering techniques
2. Explore deep learning models for intrusion detection
3. Test the models on more recent and diverse network traffic datasets
4. Implement real-time prediction capabilities

## Requirements

- Python 3.x
- Libraries: 
  - `numpy`
  - `pandas`
  - `scikit-learn`
  - `xgboost`
  - `matplotlib`
  - `seaborn`


