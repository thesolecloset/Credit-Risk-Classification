# Credit-Risk-Classification Analysis Report

## Overview of the Analysis

Using various techniques to train and evaluate a model based on loan risk. Using a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## For this challenge I analyzed the following:

Dataframe consisting of 77,536 rows of data with the following 8 columns:
* Loan Size
* Interest Rate
* Borrower Income
* Debt To Income
* Number Of Accounts
* Derogatory Marks
* Total Debt
* Loan Status

I split the data into training and testing set.  In doing so I used the training set of data to build the first initial logistic regression model.  That maodel was then used to with the testing set.  This was the process that was used to show whether a loan to the a borrower would be low risk or if it would be a high risk.

The first value counts that was taken gave the following:
0    75036(low risk)
1     2500(high risk)
0 represents the low risk loans which had 75,036 data points while, 1 represents the high risk loans which had 2,500 data points.
After doing that I resampled the data with the function RandomOverSampler which created the following value counts for both low risk and high risk loans.

0    56277(low risk)
1    56277(high risk)
I then used these data points to do the second logistic regrssion model on the testing set and produce the low risk and high risk based on these datasets.

## Results

* Machine Learning Model 1:
  * Accuracy Score - 94%(it was 100% precise in predicting the low risk loans while 87% recall in predicting the high risk loans)
  * Precision Score - 100%
  * Recall Score - 94%(it was 100% recall in predicting the low risk loans while 89% recall in predicting the high risk loans)

* Machine Learning Model 2:
  * Accuracy Score - 94%(it was 100% precise in predicting the low risk loans while 87% recall in predicting the high risk loans)
  * Precision Score - 100%
  * Recall Score - 94%(it was 100% recall in predicting the low risk loans & 100% recall in predicting the high risk loans)

## Summary

In looking at both of the logistic regression models I noticed that the model trained with the oversampled data did better.  Using this model I see that the accuracy and recall both improved while the precision percentage was able to be maintained at 100% which would minimize false positives for the high risk loans.

As a loan lending company it is imperative to minimize the number of false positives for the high risk loans which could be mistakenly plotted as healthy(low risk) loans which could ultimately cost the compnay more money.

I would recommend to the company that they use the second logistic regression model because it is more precise of the two models.  It should give you less false positives and less false negatives and improves accuracy in classifying low risk and high risk loans.

### Documented Help Received For Assignment
Received Help From Study Groups
