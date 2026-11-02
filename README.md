# Telecom Customer Churn Prediction

## Project Overview

An end-to-end machine learning project designed to predict customer churn for a telecommunications company and support customer retention decisions.

## Dataset

IBM Telco Customer Churn dataset, containing 7,043 customer records and 21 original columns.

## Technologies

Python, Pandas, NumPy, Scikit-learn, Matplotlib, Joblib and Jupyter Notebook.

## Machine Learning Pipeline

- Data exploration and preprocessing
- One-hot encoding for categorical features
- Standard scaling for numerical features
- Logistic Regression classification
- Model persistence using Joblib
- Classification threshold analysis

## Model Performance

Evaluated on 1,409 test customers using a 0.40 classification threshold.

| Metric | Result |
|---|---|
| Accuracy | 77.71% |
| Churn precision | 56.82% |
| Churn recall | 66.84% |
| Churn F1-score | Approximately 0.61 |

The model correctly identified 250 of 374 customers who churned.

## Threshold Analysis

Thresholds of 0.30, 0.40, 0.50 and 0.60 were compared to study the trade-off between precision and recall.

A 0.30 threshold achieved approximately 75.4% recall in exploratory test-set analysis. Further validation is required before selecting a new threshold for deployment.

## Project Structure

```text
telecom-churn-prediction/
├── data/
├── models/
├── results/
├── churn_analysis.ipynb
├── requirements.txt
└── README.md
```

## Future Improvements

- Select classification thresholds using validation data
- Compare additional classification algorithms
- Evaluate business costs of false positives and false negatives
- Develop an interactive prediction application

## Author

Hafsa Kouta — AI & Data Science Engineering Student