This repository cosists of the code details of the study on Severity-Index.
#Tech Debt?Predicting Severity Index in AI Software Projects

## two key contributions of this study: 
(i) it introduces a novel method for measuring the Severity Index (SI) by utilizing technical debt and code quality metrics
(ii) it identifies the most effective AI model for predicting SI in Python-based AI projects

Step 1: Pylint Radon data collection and merging from any project (in data_processing_script.ipynb).

In data_preprocessing_script_ipynb in this, python files are collected from a project. o that project Pylint and Radon is executed and thus 2 excel files are generated. These two files are needed to be merged in a single file. However, these 2 files has diffeerent columns, among them, 'file' and 'line' column exist in both files. Using those columns, these 2 files will be merged. In this code there is a 'correct' function that helps to make a same type of 'field' as this field values are in different shape in twho files then there is a 'merge' function that merge these 2 files.


Step 2: Severity Index (SI) calculation that is measured based on technical debt and software quality metrics (GenerateSI.ipynb). SI is calculated using the formula generated in the study.


Step 3: Training and testing data using various machine learning model (logistic regression, random forest, balanced random forest, XGBoost) in different orientation (cross validation, SMOTE-ENN). (in Training_Testing.ipynb)
