
# Credit Score Prediction – Project Overview

This repository consists of two main Jupyter Notebooks that walk through the end-to-end process of **generating synthetic credit data**, **exploratory analysis**, **preprocessing**, and **classification modeling** to predict credit score classes.

---

## Files

- `Data Generation.ipynb`: Creates a synthetic dataset mimicking real-world credit behavior using NumPy and pandas.
- `Preprocessing, EDA and Model.ipynb`: Contains exploratory data analysis (EDA), preprocessing, handling imbalance, and model training with performance evaluation.
- `credit_data.csv`: Final dataset used for modeling.

---

## 1. Data Generation

This notebook synthetically simulates customer credit data:

### Techniques Used:
- **NumPy random generation** for numeric variables like age, income, and EMI outflow.
- **Categorical sampling** (e.g., gender, location, occupation).
- **Custom logic for target variable**:
  - Based on risk conditions like low income + high EMI or late payments.
  - Classes: `0 = decrease`, `1 = increase`, `2 = stable`.

### Features Created:
- `age`, `gender`, `location`, `monthly_income`, `monthly_emi_outflow`
- `loan_default_count`, `payment_delay_count`, `occupation`
- `credit_score_class` (target)

---

## 2. Preprocessing, EDA and Model

This notebook handles everything from data exploration to predictive modeling.

### Preprocessing:
- **Label encoding** for categorical features (e.g., gender, occupation).
- **Train-test split** (default 80-20).
- **Class imbalance handled using SMOTE**.

### EDA Insights:
- Checked class distribution of `credit_score_class`.
- Explored distributions for income, age, EMI, etc.
- Visualizations using `matplotlib` and `seaborn`.

### Models Implemented:
- **Logistic Regression**
- **Random Forest Classifier**
- **Gradient Boosting Classifier**
- **Support Vector Classifier (SVC)**
- **XGBoost Classifier**

### Evaluation Metrics:
- **Classification report**: Precision, recall, F1-score.
- **Confusion matrix**.
- Compared models based on macro and weighted averages.

---

## Outcome Highlights

- **Best model(s)** likely achieved high accuracy by handling class imbalance effectively.
- Synthetic data generation aligned well with realistic credit patterns.
