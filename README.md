# Responsible Data Science (RDS) Project: Auditing a Loan Repayment Prediction System

## Project Overview
This project focuses on auditing the fairness and performance of an Automated Decision System (ADS) that predicts the probability of loan repayment using a Random Forest model. The primary goal is to ensure that the system provides equitable outcomes while maintaining high predictive accuracy. This auditing is essential for Home Credit to ensure their loan distribution practices are fair and unbiased.

## Motivation
Ensuring fairness and transparency in loan prediction systems is crucial for financial inclusion. The audit aims to identify any biases in the prediction model and propose ways to mitigate them. By thoroughly evaluating the model, we aim to contribute to more equitable credit decision-making processes.

## Datasets
We utilized multiple datasets provided by Home Credit Group, including:
- **application_{train|test}**: Static data from loan applications with repayment status.
- **bureau**: Client's prior credits from different financial institutions.
- **bureau_balance**: Monthly balance information for previous credits.
- **POS_CASH_balance**: Monthly balance snapshots related to consumer payments.
- **credit_card_balance**: Credit card usage data.
- **previous_application**: Data on all prior loan applications by clients.

## Methodology
### Data Preprocessing
- **Label Encoding**: For binary categories.
- **One-Hot Encoding**: For categorical variables with more than two categories.
- **Imputation**: Handling missing values carefully.

### Auditing Process
1. **Baseline Model Implementation**: Logistic Regression with regularization.
2. **ADS Model Implementation**: Random Forest with 100 trees.
3. **Performance Evaluation**: Using AUC-ROC and precision metrics.
4. **Fairness Evaluation**:
   - **False Negative Rate (FNR) Parity**: Primary metric for bias evaluation.
   - **Demographic Parity**: Additional fairness metric.
   - **Fairlearn**: Assessing and mitigating observed disparities.
5. **Explainability Tools**:
   - **SHAP and SHARP Waterfall Charts**: Visualizing individual prediction explanations.

## Results
- **Predictive Accuracy**: Evaluated using AUC-ROC.
- **Fairness Analysis**: Ensuring equitable treatment across all demographic groups, with a focus on FNR parity.
