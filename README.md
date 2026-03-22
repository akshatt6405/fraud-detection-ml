# Credit Card Fraud Detection

ML model to detect fraudulent credit card transactions 
using Logistic Regression and Random Forest on real banking data.

## Dataset
- 284,807 transactions
- Only 0.17% fraud (highly imbalanced)
- Source: Kaggle - Credit Card Fraud Detection

## What I did
- Exploratory Data Analysis (EDA)
- Visualized class imbalance
- Built Logistic Regression model
- Achieved F1 score of 0.76 for fraud detection

## Tech Stack
Python · Pandas · Scikit-learn · Matplotlib


## Results
| Model | Precision | Recall | F1 |
|-------|-----------|--------|----|
| Logistic Regression | 0.84 | 0.69 | 0.76 |
| LR Balanced | 0.05 | 0.92 | 0.10 |
| Random Forest | 0.96 | 0.74 | 0.84 |
| RF Depth=10 | 0.82 | 0.83 | 0.82 |

## Key Finding
V14 is the strongest fraud indicator — accounts for 18.6% of all model decisions.

## Next Steps
- XGBoost model
- Push F1 above 0.85
- Final model comparison
