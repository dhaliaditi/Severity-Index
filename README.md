# Tech Debt? Predicting Severity Index in AI Software Projects
This repository cosists of the code details of the study on Severity-Index.
Two key contributions of this study: 
i) It introduces a novel method for measuring the Severity Index (SI) by utilizing technical debt and code quality metrics
ii) It identifies the most effective AI model for predicting SI in Python based AI projects

## Step 1: Pylint and Radon data collection and merging from any project
- Run the script: "data_processing_script.ipynb" on the target source code.
- This script runs Pylint and Radon on the given source code it generates 2 excel files containing the output separately from Pyling and Radon, and another file combining the two.

## Step 2: Measure Severity Index (SI) 
- Run the script "GenerateSI.ipynb" by providing the third output file (the merged one).
- This script will generate a file "training.csv" containing SI and dependent variables in the data.

## Step 3: Training and testing machine learning models (Logistic Regression, Random Forest, Balanced Random Forest, XGBoost)
- The trainig is done on different settings of the data combining cross validation and SMOTE-ENN.
- Run the script Training_Testing.ipynb to observe the performance of the models.
