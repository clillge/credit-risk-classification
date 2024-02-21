# credit-risk-classification

## Overview of the Analysis

The purpose the this analysis was to train and evaluate a model based on various factors relating to loan risk.

These factors are:
  * The size of the loan
  * The interest rate of the loan
  * The income of the borrower
  * The borrower's debt to income ratio
  * The borrower's total debt
  * The number of accounts of the borrower
  * The number of "Derogatory Marks" on these accounts

The steps taken in the machine learning process are as follows:
  1. Separate the value we're looking for (in this case the loan status, which classifies the loan as a healthy loan or a high-risk loan) from the rest of the data that leads to its' classification.
  2. Create the training and testing datasets from the original data.
  3. Create a Logistic Regression Model using the training data and make predictions on the testing data from this model.
  4. Generate a confusion matrix and print a classification report based on the prior prediction.

The Logistic Regression Model in this case is simply the process used to predict the probability of the loan status given our input variables. It takes the training data to learn the impact each variable has on the output, weighs those variables depending on said impact, and uses that to predict future outputs.

Given those weightings and assumptions made by the model, we can then use it to predict the output on our testing data and find how well it performs. From this we create our confusion matrix and classification report as a sort of grade regarding the model's performance. This allows us to gauge how useful the model will be if used to predict real-world loan statuses.

## Results

* Machine Learning Model:
  * Accuracy: 92% for precision, 95% for recall across both types of loans.
  * Precision: 100% for healthy loans, 85% for high-risk loans.
  * Recall: 99% for healthy loans, 91% for high-risk loans.

## Summary

Due to the high precision when predicting healthy loans this model would work great for predicting healthy loans consistently and with a high degree of confidence. With a precision of nearly 100% and a recall of 99% it is very well trained for this purpose. However, the model is much less effective in predicting high-risk loans, with a precision of only 85% and a recall of 91%. For this reason I would suggest using a different model when attempting to predict high-risk loans.