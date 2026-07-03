# 💳 Credit Card Fraud Detection using Machine Learning

An end-to-end Machine Learning project to detect fraudulent credit card transactions using multiple classification models, with a focus on handling severe class imbalance and selecting the most suitable model for real-world fraud detection.

---

## 📌 Project Overview

Credit card fraud is a major challenge for financial institutions, leading to financial losses and reduced customer trust. Detecting fraudulent transactions is difficult because fraud represents only a tiny fraction of all transactions.

This project develops a complete Machine Learning pipeline to identify fraudulent transactions using historical transaction data.

Rather than relying only on Accuracy, multiple evaluation metrics including Precision, Recall, F1-score, ROC-AUC and Precision-Recall curves are used to compare models and understand the trade-offs between fraud detection capability and customer experience.

---

## 🎯 Problem Statement

How can fraudulent credit card transactions be accurately detected while minimizing false alarms on genuine customer transactions?

Since fraudulent transactions account for only **0.172%** of the dataset, traditional evaluation metrics such as Accuracy become misleading. This project focuses on selecting a model that balances fraud detection (Recall) with minimizing unnecessary transaction blocks (Precision).

---

## 📊 Dataset

**Dataset:** Credit Card Fraud Detection Dataset (Kaggle)

**Link:** https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

- **Total Transactions:** 284,807
- **Fraudulent Transactions:** 492
- **Fraud Rate:** 0.172%
- **Features:** 30
- **Target Variable:** Class
  - **0 → Genuine Transaction**
  - **1 → Fraudulent Transaction**

Most input variables (V1–V28) are anonymized using Principal Component Analysis (PCA) to preserve customer privacy.

---

## 🏗️ Machine Learning Workflow

The project follows the workflow below.

```text
Credit Card Transaction Dataset
              │
              ▼
Data Cleaning
              │
              ▼
Exploratory Data Analysis
              │
              ▼
Data Preprocessing
              │
              ▼
Train-Test Split
              │
              ▼
Feature Scaling
              │
              ▼
Model Development
(Logistic Regression,
Decision Tree,
Random Forest,
XGBoost)
              │
              ▼
Hyperparameter Tuning
              │
              ▼
Model Evaluation
              │
              ▼
Feature Importance
              │
              ▼
Final Model Selection
```

---

## 🤖 Machine Learning Models

The following models were implemented and compared:

- Logistic Regression (Baseline)
- Logistic Regression with SMOTE
- Decision Tree
- Random Forest
- XGBoost
- Hyperparameter Tuned XGBoost

---

## 📈 Model Performance

| Model | Accuracy | Precision | Recall | F1 Score |
|--------|---------:|----------:|-------:|---------:|
| Logistic Regression | 99.91% | 84.85% | 58.95% | 69.57% |
| Logistic Regression + SMOTE | 97.36% | 5.30% | **87.37%** | 10.00% |
| Decision Tree | 99.90% | 72.04% | 70.53% | 71.28% |
| Random Forest | 99.95% | **97.18%** | 72.63% | 83.13% |
| XGBoost | 99.95% | 94.52% | 72.63% | 82.14% |
| ⭐ Tuned XGBoost | **99.95%** | **96.00%** | **75.79%** | **84.71%** |

The tuned XGBoost model achieved the highest F1-score and provided the best balance between detecting fraud and minimizing false positives.

---

## 📊 Model Evaluation

The models were evaluated using multiple performance metrics instead of relying solely on Accuracy.

Evaluation techniques include:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC-AUC Curve
- Precision-Recall Curve
- Feature Importance

---

## 🌟 Key Insights

- The dataset exhibits **extreme class imbalance**, making Accuracy an unreliable evaluation metric.
- Applying **SMOTE** significantly improved Recall but introduced a large number of false positives.
- Ensemble models (Random Forest and XGBoost) substantially outperformed individual models.
- Hyperparameter tuning improved XGBoost performance, increasing the F1-score from **82.14%** to **84.71%**.
- PCA-transformed features such as **V14**, **V12**, **V10**, and **V17** consistently showed high importance across ensemble models.

---

## 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn (SMOTE)
- XGBoost
- Google Colab
- Git & GitHub

---
