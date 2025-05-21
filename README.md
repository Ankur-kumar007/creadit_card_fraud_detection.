# creadit_card_fraud_detection.
# 💳 Credit Card Fraud Detection

This project focuses on detecting fraudulent transactions using machine learning techniques. It uses anonymized credit card transaction data and trains a model to classify whether a given transaction is fraudulent or not.

## 📌 Table of Contents
- [Dataset](#dataset)
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Model Training](#model-training)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [How to Run](#how-to-run)
- [Future Improvements](#future-improvements)
- [License](#license)

---

## 📂 Dataset

- The dataset used is the **Credit Card Fraud Detection dataset** available on [Kaggle](https://www.kaggle.com/mlg-ulb/creditcardfraud).
- It contains **284,807 transactions**, with **492 cases of fraud**.
- Features are numerical and PCA-transformed for privacy (`V1` to `V28`) plus `Time`, `Amount`, and the target `Class` (1 = fraud, 0 = not fraud).

---

## 🧠 Project Overview

- **Goal:** Accurately detect fraudulent transactions while minimizing false positives.
- **Challenges:** Imbalanced dataset (fraud cases are ~0.17% of all transactions).
- **Solution:** Applied preprocessing, data balancing (e.g., SMOTE or undersampling), and trained various ML models.

---

## 🛠️ Technologies Used

- Python 🐍
- Scikit-learn
- LightGBM / XGBoost (if used)
- Pandas, NumPy
- Matplotlib, Seaborn (for visualization)

---

## 📈 Model Training

- Preprocessing:
  - Handled class imbalance using [SMOTE / Random Undersampling].
  - Scaled the `Amount` and `Time` features using `StandardScaler`.
- Models Trained:
  - Logistic Regression
  - Random Forest
  - LightGBM (if used)
- Cross-validated on stratified folds for robustness.

---

## 📊 Evaluation Metrics

Given the class imbalance, standard accuracy isn't useful. Metrics used:
- **Precision**
- **Recall**
- **F1-score**
- **ROC-AUC**
- **Confusion Matrix**

---

## ✅ Results

| Model              | Precision | Recall | F1-score | ROC-AUC |
|-------------------|-----------|--------|----------|---------|
| Logistic Regression | 0.91      | 0.62   | 0.73     | 0.95    |
| Random Forest       | 0.97      | 0.83   | 0.89     | 0.99    |
| LightGBM            | 0.96      | 0.87   | 0.91     | 0.99    |

*(Replace with actual values from your model)*

---

## 🚀 How to Run

1. **Clone the repository:**
```bash
git clone https://github.com/your-username/credit-card-fraud-detection.git
cd credit-card-fraud-detection
