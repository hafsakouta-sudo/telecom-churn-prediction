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

The Logistic Regression model was trained using a 60% training, 20% validation, and 20% test split.

A classification threshold of 0.30 was selected using validation data to prioritize identifying customers at risk of churn.

### Test Results

Evaluated on 1,409 test customers.

| Metric | Result |
|---|---|
| Accuracy | 75.37% |
| Churn precision | 52.51% |
| Churn recall | 75.40% |
| Churn F1-score | 0.62 |
| Classification threshold | 0.30 |

### Confusion Matrix

| | Predicted No | Predicted Yes |
|---|---:|---:|
| Actual No | 780 | 255 |
| Actual Yes | 92 | 282 |

The model correctly identified 282 of 374 customers who churned.

The selected threshold prioritizes churn recall, accepting more false positives to reduce the number of missed churners.

**Evaluation note:** The test set had been examined during earlier development, so these results represent a revised holdout evaluation rather than a completely independent final assessment.

## Threshold Analysis


## Threshold Analysis

Classification thresholds of 0.30, 0.40, 0.50, and 0.60 were compared using the validation dataset to evaluate the trade-off between precision and recall.

A threshold of 0.30 was selected because the business objective is to identify as many customers at risk of churn as possible, even at the cost of additional false positives.

On the validation dataset, this threshold achieved approximately 75% churn recall and 54% precision.

Using the selected threshold, the model achieved 75.37% accuracy and 75.40% churn recall on the test dataset.

These results are exploratory because the test set had been examined during earlier development. Further evaluation on new, independent data would be needed before deployment.


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