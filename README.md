# ESG Portfolio Risk Management (Machine Learning)

This project builds a machine learning pipeline to classify ESG portfolio risk (high-risk vs low-risk) using ESG score stability and macroeconomic indicators.

## What the notebook does
- Loads ESG performance time series for multiple companies plus macroeconomic data (inflation, interest rate, GDP growth).
- Computes rolling 30-day ESG volatility for each company. Higher volatility = higher ESG instability = considered higher risk.
- Creates a binary risk label:
  - 1 = high risk (above median volatility)
  - 0 = low risk
- Handles class imbalance by oversampling the high-risk class.
- Trains and evaluates multiple classification models:
  - Random Forest
  - Gradient Boosting
  - XGBoost
  - Logistic Regression
  - Support Vector Machine (SVM)
  - Neural Network (MLP)
  - AdaBoost
- Compares models using accuracy, precision, recall, F1-score, confusion matrix, and cross-validation.
- Extracts feature importance (which signals drive risk).
- Visualizes:
  - ESG score trends over time
  - Volatility trends
  - Correlation between ESG metrics and macroeconomic indicators

## Why this matters
- Treats ESG instability as an early risk signal.
- Helps with portfolio risk screening and ESG-adjusted risk management.

## Data privacy
The original dataset includes confidential ESG scores and macroeconomic indicators and is **not** included in this repository.

To reproduce:
1. Provide your own ESG time-series data (company ESG scores over time).
2. Include macro factors like inflation, interest rate, GDP growth.
3. Run the notebook and regenerate the rolling-volatility and `Risk` labels.

Raw data files (`.csv`, `.xlsx`) are intentionally excluded.
