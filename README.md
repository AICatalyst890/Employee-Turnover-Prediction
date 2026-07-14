# Employee Turnover Prediction

A streamlined machine learning workflow implementing and benchmarking regularized Logistic Regression models to predict employee attrition.

---

## 📊 Pipeline Workflow

1. **Exploratory Visualization:** Analyzed the relationship between `Job_Satisfaction` and `Employee_Turnover` using a Seaborn bar plot.
2. **Data Split:** Partitioned the dataset using an 80/20 train-test split (`random_state=42`).
3. **Model Training:** Evaluated four variations of Logistic Regression:
* **Baseline:** Standard unpenalized model (`max_iter=500`).
* **Lasso ($L_1$):** Configured with `C=0.5` and `solver="liblinear"`.
* **Ridge ($L_2$):** Configured with `C=0.2` and `solver="liblinear"`.
* **ElasticNet:** Configured with `C=0.5`, `l1_ratio=0.8`, and `solver="saga"`.



---

## 📈 Model Performance Benchmark

Evaluating the test set (145 retention and 125 turnover instances) yielded the following exact metrics:

| Model Hierarchy | Accuracy | Precision (Class 1) | Recall (Class 1) | F1-Score (Class 1) |
| --- | --- | --- | --- | --- |
| **Lasso ($L_1$ Regularization) 🏆** | **87.04%** | **88.14%** | **83.00%** | **86.00%** |
| **ElasticNet** | 86.30% | 87.93% | 82.00% | 85.00% |
| **Baseline Logistic Regression** | 85.93% | 87.18% | 82.00% | 84.00% |
| **Ridge ($L_2$ Regularization)** | 85.19% | 84.55% | **83.00%** | 84.00% |

---

## 🎯 Key Insights

* **Lasso ($L_1$) is the Champion Model:** Outperformed all configurations by successfully driving non-impactful feature coefficients to zero, resulting in the best generalizability.
* **Optimal Business Balance:** Achieved **88.14% Precision** (minimizing costly "false alarms" on retention incentives) and **83.00% Recall** (capturing the vast majority of true flight-risk employees).

---

## 📂 Repository Structure

* `employeeTurnover.ipynb` — Main Jupyter Notebook with data visualization, training, and evaluation.
* `employee_turnover.csv` — Anonymized historical workforce dataset.
* `requirements.txt` — Project environment dependencies.
* `README.md` — Project summary and benchmarks.