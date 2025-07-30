# Maternal Health & High-Risk Pregnancy Prediction

A machine learning project to predict high-risk pregnancies using the [Maternal Health and High-Risk Pregnancy Dataset](https://www.kaggle.com/datasets/myct001/maternal-health-risk-data-set).

## 📋 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Features](#features)
- [Preprocessing](#preprocessing)
- [Feature Engineering](#feature-engineering)
- [Modeling](#modeling)
- [Results](#results)
- [Usage](#usage)
- [Future Work](#future-work)
- [Credits](#credits)

---

## 📝 Overview

This project aims to identify and classify pregnancies at high risk of complications using clinical, demographic, and lifestyle indicators. The goal is to support improved monitoring and intervention for maternal health.

---

## 📊 Dataset

- Source: [Kaggle, Maternal Health Risk Data Set](https://www.kaggle.com/datasets/myct001/maternal-health-risk-data-set)
- Features: Age, Systolic BP, Diastolic, Blood Sugar (BS), Body Temperature, BMI, Heart Rate, Mental Health, Previous Complications, Preexisting Diabetes, Gestational Diabetes, and others
- Target: `Risk Level` (0 = low, 1 = high)

---

## 🛠️ Preprocessing

- Removed rows with missing or invalid target values
- Imputed missing numeric values with median
- Capped or flagged outliers based on clinical knowledge
- Encoded categorical and binary features

---

## 🔬 Feature Engineering

- Created interaction & aggregate features:
    - `BP_Product` = Systolic BP × Diastolic
    - `Pulse_Pressure` = Systolic BP – Diastolic
    - `BS_BMI` = Blood Sugar × BMI
    - Flags: `High_BP`, `High_BS`, `Obese`
    - Aggregates: `Any_Diabetes`, `Complicated_History`
- Applied log transformations for skewed data

---

## 🤖 Modeling

- **Classifiers used**:
    - Logistic Regression
    - Random Forest
    - Gradient Boosting
    - Support Vector Machines (Linear, RBF)

- **Evaluation metrics**:
    - Accuracy, F1-score, ROC-AUC
    - Confusion Matrix
    - Feature Importance

---

## 📈 Results

| Model               | Accuracy | F1-score | ROC-AUC |
|---------------------|----------|----------|---------|
| Logistic Regression | 0.97     | 0.97     | 0.997   |
| Random Forest       | 0.99     | 0.98     | 1.000   |
| Gradient Boosting   | 0.99     | 0.99     | 1.000   |
| SVM (Linear)        | 0.97     | 0.96     | 0.995   |
| SVM (RBF)           | 0.71     | 0.53     | 0.75    |

- **Best Models**: Gradient Boosting & Random Forest

---

## 🚀 Usage

1. Clone the repo:
    ```bash
git clone https://github.com/YOURUSERNAME/your-maternal-health-risk.git
cd your-maternal-health-risk
    ```

2. Install dependencies:
    ```bash
pip install -r requirements.txt
    ```

3. Run the pipeline:
    ```bash
python main.py
    ```
   or run the provided Jupyter Notebook for full workflow and visuals.

---

## 🔭 Future Work

- Hyperparameter tuning
- Additional clinical feature engineering
- SHAP/LIME interpretability
- Model deployment (Streamlit app or API)

---

## 🙏 Credits

- Dataset: Kaggle & A. Abhishek
- Project by [Ali ABdollahi]
- 
