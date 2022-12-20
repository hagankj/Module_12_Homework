# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.<br>
The purpose of this analysis was to develop a model that can predict which loans are 'healthy', and which loans are high-risk and likely to default.
* Explain what financial information the data was on, and what you needed to predict.<br>
The *lending_data* file included several characteristics to help predict healthy and potential default outcomes. Characteristics included:
  - Loan size
  - Interest rate of the loan
  - Income for the borrower
  - Debt to income ratio
  - Number of accounts
  - Derogatory credit remarks
  - Total debt
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).<br>
The variable we were trying to predict is the loan status - whether it is 'healthy' or 'defaulted'.
* Describe the stages of the machine learning process you went through as part of this analysis.<br>
First, I needed to split the data into two groups. The 'y', which I referred to as the 'target' group, and 'X', which I called 'features'. I then reviewed the number of healthy loans and high-risk loans to understand the data split. Using the given data, I the split the details into testing data and training data both for the features ('X') and target ('y') details. Using the training data, I developed a logistic regression model. I think used the model to make predictions against the training set and confirmed the accuracy, which was roughly 95%. This means that my model correctly assigned a 'healthy' or 'high-risk' designation to the 95% of the data included in the training set.<br>
Second, we resampled the data in an effort to rebalance the health/high-risk classification in order to help validate the outputs from the initial model. 

* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).<br>
Most of the detail surrounding the methods used are illustrated above; however, to be specific I used logistic regression, and the radom over sampler to distribute '0' and '1' evenly.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Description of Model 1 Accuracy, Precision, and Recall scores.
<br>
    - *Accuracy*: The model accurately predicted the '0' or '1' outcome 95% of the time<br>
    - *Precision*: Out of all the loans the model predicted would default, the model correctly predicted 85% of the high-risk loans<br>
    - *Recall*: The recall score was equally high, correctly prediting the outcome of the loan 91% of the time.

* Machine Learning Model 2:
  * Description of Model 2 Accuracy, Precision, and Recall scores.
<br>
    - *Accuracy*: The model accurately predicted the '0' or '1' outcome 99% of the time<br>
    - *Precision*: Out of all the loans the model predicted would default, the model correctly predicted 84% of the high-risk loans<br>
    - *Recall*: The recall score was equally high, correctly prediting the outcome of the loan 99% of the time.


## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:<br>
Between the two models, the oversampled data appears to be better. One cause for pause is the accuracy measure, which is 99%. It is far more important to predict the '1' because failing do so would mean lending funds to an individual who will default and fail to pay back.
If you do not recommend any of the models, please justify your reasoning.
