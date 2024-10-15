# Module 12 Report

## Overview of the Analysis

* Purpose of the Analysis:
The purpose of this analysis is to use machine learning to predict credit risk based on financial data. By analyzing loan statuses and other related financial variables, the goal is to determine which loans are high-risk versus healthy. This will help financial institutions identify loans that are likely to default, enabling better risk management.
##
* Explain what financial information the data was on, and what you needed to predict:
The dataset used in this analysis contains various financial features about loans, such as loan amount, interest rate, and borrower information. The primary variable to predict is loan_status, which can either be:

0 – indicating a healthy loan.

1 – indicating a high-risk loan.

The model aims to predict whether a loan is high-risk or healthy based on the other features.
##
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`):

Healthy: 75036

High-Risk: 2500

There are far more healthy loans than high-risk loans.
##
* Describe the stages of the machine learning process you went through as part of this analysis:
1. Data Preparation:
The dataset was split into features (X) and labels (y). The features include various loan characteristics, while the labels are the loan_status values.
The data was further split into training (75%) and testing (25%) sets to ensure that the model could be trained and evaluated on separate data.
2. Model Selection:
A Logistic Regression model was selected due to its simplicity and effectiveness for binary classification tasks.
3. Model Training:
The Logistic Regression model was trained using the training data (X_train and y_train).
4. Model Evaluation:
After training, the model was used to make predictions on the testing data (X_test).
The model's performance was evaluated using the confusion matrix and classification report, which provide metrics like accuracy, precision, recall, and F1-score for both classes (0 and 1).
##

## Results

* Machine Learning Model 1:
  
    Accuracy: 99%
  
    Precision:
  
    Class 0 (healthy loan): 1.00
  
    Class 1 (high-risk loan): 0.84
  
    Recall:
  
    Class 0 (healthy loan): 0.99
  
    Class 1 (high-risk loan): 0.94
  
    F1-Score:
  
    Class 0: 1.00
  
    Class 1: 0.89

## Summary
##
Best Performing Model: The Logistic Regression model performed exceptionally well, achieving an overall accuracy of 99%. It performed perfectly on classifying healthy loans (class 0), with precision, recall, and F1-scores of 1.00 for that class.

High-Risk Loan Prediction: For high-risk loans (class 1), the model had a slightly lower precision of 0.84 and an F1-score of 0.89, but it managed to identify 94% of actual high-risk loans (recall), which is a solid result for this type of model.

Recommendation: The model shows strong performance in predicting both healthy and high-risk loans. Given that financial institutions may prioritize identifying high-risk loans to minimize default risk, this model's high recall (0.94) for high-risk loans makes it a reliable option. While the precision for high-risk loans could be improved, the model is highly effective in identifying risky loans and would likely serve as a useful tool for credit risk management.

Consideration of the Problem: In this case, predicting the 1s (high-risk loans) is more important because missing a high-risk loan could result in financial losses. The model's ability to capture 94% of these loans suggests that it can be beneficial for reducing risk.
