# Credit Card Fraud Detection

ML model to detect fraudulent credit card transactions using 
Logistic Regression, Random Forest and XGBoost on real banking data.

## Dataset
- 284,807 transactions
- Only 0.17% fraud (highly imbalanced)
- Source: Kaggle - Credit Card Fraud Detection

## What I did
- Exploratory Data Analysis (EDA)
- Visualized class imbalance problem
- Built and compared 5 ML models
- Analyzed feature importance across 2 algorithms
- Evaluated using Confusion Matrix

## Tech Stack
Python · Pandas · Scikit-learn · XGBoost · Matplotlib

## Results
| Model | Precision | Recall | F1 |
|-------|-----------|--------|----|
| Logistic Regression (unbalanced) | 0.84 | 0.69 | 0.76 |
| Logistic Regression (balanced) | 0.05 | 0.92 | 0.10 |
| Random Forest (balanced) | 0.96 | 0.74 | 0.84 |
| Random Forest (max_depth=10) | 0.82 | 0.83 | 0.82 |
| **XGBoost** | **0.89** | **0.83** | **0.86** |

## Best Model — XGBoost
- Precision: 0.89
- Recall: 0.83
- F1 Score: 0.86

## Confusion Matrix (XGBoost)
| | Predicted Normal | Predicted Fraud |
|--|-----------------|----------------|
| Actual Normal | 56,854  | 10  |
| Actual Fraud | 17  | 81  |

- 81 out of 98 frauds correctly caught
- Only 10 false alarms out of 56,864 normal transactions

## Key Findings
- V14 is the dominant fraud signal
  - Random Forest: 18.6% importance
  - XGBoost: 61.2% importance
- Top 5 features capture 59% of Random Forest decisions
- Transaction Amount appeared in XGBoost top 10 — consistent 
  with real fraud behavior where criminals test cards with small amounts

## Key Insight
Accuracy is a misleading metric for imbalanced datasets. 
A model predicting "normal" for everything achieves 99.83% accuracy 
but catches zero fraud. F1 score is the correct metric here.
