# Module 20: Credit Risk Classification
## Table of Contents
* [About](#about)
* [Tools](#tools)
* [Analysis](#analysis)
* [Results](#results)
* [Summary](#summary)
## About
In this project, I assessed logistic regression models' performance in predicting customer loan worthiness using loan size, interest rate, borrower income, debt-to-income ratio, number of credit accounts, derogatory marks, and total debt as predictive factors.
## Tools
* Python
* PANDAS
* pathlib
* sklearn.metrics
## Analysis
The data was initially split into the target and feature variables, followed by a train-test split. A logistic regression model was applied to the test portion, resulting in predictions. Evaluation metrics, including balanced accuracy score, confusion matrix, and classification report, were computed to assess the model's performance.

Observing an imbalanced distribution of healthy and high-risk loans (75,036 vs. 2,500), random oversampling (using RandomOverSampler from imblearn.over_sampling) was employed to balance the classes. The same logistic regression model and evaluation were repeated on the oversampled data.
## Results
**Logistic Regression on Training Data:**  
* Balanced accuracy score: 94%  
* Precision for healthy loans: 99.57%  
* Recall for healthy loans: 99.64%  
* Precision for high-risk loans: 87%  
* Recall for high-risk loans: 89%  

**Oversampled Data Logistic Regression:**  
* Balanced accuracy score: 99.59%  
* Precision for healthy loans: 99.51%  
* Recall for healthy loans: 99.98%  
* Precision for high-risk loans: 87%  
* Recall for high-risk loans: 99.68%  

## Summary
**Oversampled Data Logistic Regression** outperforms the model without oversampling. While predictions for healthy loans are consistent between both models, oversampling significantly enhances high-risk loan recall (99.68% vs. 89%). This improvement is crucial for reducing the number of risky loans approved, prioritizing loan approval for creditworthy customers over high precision for high-risk loans.






