This repository cosists of the code details of the study on Severity-Index.
#Tech Debt?Predicting Severity Index in AI Software Projects

## two key contributions of this study: 
(i) it introduces a novel method for measuring the Severity Index (SI) by utilizing technical debt and code quality metrics
(ii) it identifies the most effective AI model for predicting SI in Python-based AI projects

Step 1: Pylint Radon data collection and merging from any project (in data_processing_script.ipynb).
Step 2: Severity Index (SI) calculation that is measured based on technical debt and software quality metrics (GenerateSI.ipynb).
Step 3: Training and testing data using various machine learning model (logistic regression, random forest, balanced random forest, XGBoost) in different orientation (cross validation, SMOTE-ENN). (in Training_Testing.ipynb)
