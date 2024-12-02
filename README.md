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


## Answering Research Questions (RQs): It contains scripts and results
## Answering RQ1: 
- Input: 2group_relationFinding.csv
- output: 2group_relation.xlsx. 
- Input file was generated using the training and testing data, keeping only columns (symbol,category, complexity_score, comments, multi, blank, h1,h2,N1,N2,vocabulary, length, calculated length, volume, difficulty,effort, time, bugs, maintainability, version, Risk_Group) representing prominent features.
- Using this excel we generated 2 graphs representing Categories of Technical Debts in our dataset and Low-High Category Distribution Across Severity Groups.

## Answering RQ2:
- Input: training.csv or testing.csv
- Output: severity_range (severity ranges in different project based on low and high severity)

## Answering RQ3:
  - Input: 2group_relation.xlsx (gained from RQ1 output)
  - Output: 4 radar chart representing Comparison of metric influences in individual project, 1 bar chart Comparing Metrics for High and Low Severity (Anjani, ChuanhuGPT, Maltrail, Recommenders)

## Answering RQ4:
- Step 3 (previously mentioned) contains the script that will generate the result of RQ4.
- Summary of the result were mentioned in a table and analysed in the submitted paper.
