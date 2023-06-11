# credit-risk-classification

## Overview of the Analysis

I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers. This included reviewing factors such as loan size, interest rate, borrower income, debt to income ratio, number of accounts, derogatory marks, and total debt of borrowers to predict whether they would have a healthy loan or a high-risk loan. Our goal is to increase the number of healthy loans and limit the number of high-risk loans provided. 

The historical dataset included 75,036 healthy loans and 2500 high-risk loans. In my first attempt, I split the data into training and testing data and fit and trained a Logistic Regression model to the training data to make predictions. While the balanced accuracy score of this model was high at 95.2%, the confusion matrix and the classification report revealed an oversampling of healthy loans (18,765) compared to high-risk loans (619) in the data. 

As a result, I used the RandomOverSampler to resmaple the data, which led to the same number (112,542) of healthy and high-risky loans. This oversample led to an increase in the balanced accuracy score of the logistic regression model from 95.2% to ~99.4%. While precision scores have stayed relatively the same, the recall score for high-risk loans has increased and is now the same as that of healthy loans at 99%. This means that the ratio of true positives compared to true positives and false negatives combined is the same for both healthy and high-risk loans using oversampled data.

## Results

Here you will find the balanced accuracy scores and the precision and recall scores of both machine learning models.

* Machine Learning Model 1:
  - Accuracy Score: ~99.2% 
  - Balanced Accuracy Score: 95.2% 
  - Precision Score:
    - Healthy Loans: 100%
    - High-Risk Loans: 85%
  - Recall Score: 
    - Healthy Loans: 99%
    - High-Risk Loans: 91%
  

* Machine Learning Model 2 (Oversampling):
  - Accuracy Score: ~99.4%
  - Balanced Accuracy Score: ~99.4%
  - Precision Score:
    - Healthy Loans: 100%
    - High-Risk Loans: 84%
  - Recall Score:
    - Healthy Loans: 99%
    - High-Risk Loans: 99%
  
## Summary

The second machine learning model (oversampling) seems to perform best as it has a higher balanced accuracy score - it will be correct 99.4% of the time. It results in only a slightly higher number of false negatives, while substantially cutting down the number of false positives - therefore, being better at weeding out high-risk borrowers. If the bank's goal is to increase the number of healthy loans provided while minimizing the number of high-risk loans provided then the second model is the better option.
