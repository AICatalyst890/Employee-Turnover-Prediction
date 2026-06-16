# Employee Turnover Prediction

An end-to-end machine learning project designed to predict employee attrition using classification models. This project implements baseline logistic regression along with L1 (Lasso), L2 (Ridge), and ElasticNet regularization techniques to identify key drivers of employee turnover and improve model generalization.

## 📊 Project Overview
Predicting employee turnover helps organizations proactively address retention challenges. This repository explores data preprocessing and regularized linear classification models to predict whether an employee is likely to leave or stay.

### Model Performance Summary
Based on our test set evaluations, the **Lasso (L1) Regularization** model yielded the highest accuracy by effectively filtering out noisy features:

| Model | Accuracy | Precision (Class 1) | Recall (Class 1) | F1-Score (Class 1) |
| :--- | :---: | :---: | :---: | :---: |
| **Lasso (L1)** | **87.04%** | **88.14%** | **83.00%** | **0.86** |
| **ElasticNet** | 86.30% | 87.93% | 82.00% | 0.85 |
| **Baseline (Logistic)** | 85.93% | 87.18% | 82.00% | 0.84 |
| **Ridge (L2)** | 85.19% | 84.55% | 83.00% | 0.84 |

## 🚀 Features
- **Data Preprocessing & Cleaning:** Handling missing values, encoding categorical variables, and feature scaling.
- **Regularization Analysis:** Comparison between Baseline Logistic Regression, Lasso, Ridge, and ElasticNet models.
- **Performance Evaluation:** Comprehensive breakdown using Accuracy, Precision, Recall, and F1-Scores.

## 🛠️ Installation & Setup

1. **Clone the repository:**
git clone https://github.com/AICatalyst/Employee-Turnover-Prediction.git
cd Employee-Turnover-Prediction