# Credit-Default-Risk

## Overview
This project aims to predict credit card defaults using machine learning. The dataset contains historical data of 30,000 Taiwanese credit card clients, including demographic features, payment history, billing statements, and repayment behavior. The goal is to build a predictive model to identify high-risk clients and help financial institutions mitigate losses.

## Dataset Details

**Source**: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients)

### Variables:

* **Demographic Features:** Credit limit (`LIMIT_BAL`), gender (`SEX`), education (`EDUCATION`), marital status (`MARRIAGE`), age (`AGE`).

* **Payment History:** Repayment status for the past 6 months (`PAY_0` to `PAY_6`).

* **Billing Statements:** Bill amounts for the past 6 months (`BILL_AMT1` to `BILL_AMT6`).

* **Payment Amounts:** Amounts paid in the past 6 months (`PAY_AMT1` to `PAY_AMT6`).

* **Target Variable:** DEFAULT (binary indicator: 1 = default, 0 = non-default).

### Preprocessing

* **Handling Missing Values:** No missing values detected.

* **Categorical Variables:**

**EDUCATION:** Categories 0, 5, 6 merged into "Others".

**MARRIAGE:** Category 0 merged into "Others".

* **Feature Engineering:**

Created `TOTAL_BILL_AMT` (sum of all bill amounts).

Created `TOTAL_PAY_AMT` (sum of all payment amounts).


## Problem Statement
Traditional credit risk assessment methods lack precision, leading to financial losses for lenders and missed opportunities with low-risk clients. A data-driven approach is needed to predict defaults accurately.


## Objective
Develop a machine learning model to:

* Identify clients at high risk of defaulting.

* Enable institutions to optimize credit limits, improve collections, and reduce defaults.


## Methodology

### Exploratory Data Analysis (EDA)

* Clients with lower credit limits and delayed payment histories are more likely to default.
* Higher total bill amounts correlate with higher default risk.


### Econometric Analysis
Explored the Logistic Regression model for checking the Statistical significance of the variables and observe the direction of causalty of the model.


### Machine Learning
* Used various ML models like Logistic Regression, Lasso and Elastic Regression
*  Essemble Learning was also used by combining Support Vector Machine Classifier, Random Forest Classifier and Voting Classifier.
*  Also explored Neural Networks and checked how well can they work on our data.


## Future Work

### Model Development:

* Use different models like XGBost
* Address class imbalance using SMOTE or class weighting.

### Feature Engineering:

* Create ratios (e.g., PAY_AMT/BILL_AMT) to capture repayment behavior.
* Analyze temporal trends in payment delays.

### Evaluation:

* Use metrics like AUC-ROC, precision-recall, and F1-score.
* Perform cross-validation to ensure robustness.

### Deployment:

* Build an API for real-time predictions.
* Create a dashboard for risk visualization.


## Dependencies
Python 3.7+

**Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, tensorflow.


## Contributor
Utkarsh Bhardwaj
Publish Date: 28th Feburary, 2025
Contact: ubhardwaj284@gmail.com
[LinkedIn](https://www.linkedin.com/in/utkarsh284/) | [GitHub](https://github.com/utkarsh-284)
