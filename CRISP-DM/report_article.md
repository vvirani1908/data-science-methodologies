# Predicting Telco Customer Churn with CRISP-DM

## Problem and business value

Customer churn reduces recurring revenue and makes acquisition spending less effective. This project applies CRISP-DM to build a model that ranks customers by churn risk so a retention team can prioritize outreach.

## Method

The IBM Telco Customer Churn dataset was profiled for data types, missing values, duplicates, class balance, and contract-related patterns. The identifier was removed, `TotalCharges` was converted to numeric, missing values were imputed, and categorical variables were one-hot encoded. Logistic regression with class weighting was evaluated using a stratified holdout set.

## Results and deployment

ROC-AUC, precision, recall, F1, and a confusion matrix are reported in the notebook. The recommended deployment is weekly batch scoring followed by human-reviewed retention outreach. Thresholds should reflect campaign cost and missed-churn cost.

## Limitations

The model identifies association, not causal treatment effect. Future work should use time-based validation, drift monitoring, and uplift experiments.

## Methodology traceability

The project follows CRISP-DM as an iterative process rather than a one-way checklist. Business questions determine the target and evaluation criteria; data understanding identifies quality and bias risks; preparation is placed inside a pipeline to prevent leakage; modeling compares interpretable and nonlinear approaches; evaluation uses multiple metrics; and deployment includes monitoring and human review.

## Practical implications

The output should be treated as a ranked prioritization list. A retention manager can use probability bands to decide which customers receive educational support, plan changes, or a human call. The business should run an experiment to measure incremental retention rather than assuming that a high-risk customer will respond to every offer.

## Reproducibility

The notebook records the public dataset URL, random seed, preprocessing steps, train/test split, model settings, metrics, and limitations. A production version would additionally record model versions, data timestamps, and approval decisions.
