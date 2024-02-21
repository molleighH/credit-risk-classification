# Credit Risk Classification
## Overview of the Analysis 
Explain the purpose of this analysis:
* The purpose of this activity is to use various techniques to train and evaluate a model based on loan risk. The activity uses a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers and classify the credit risk predictions. 
* The target finiancial information in the data is the loan status. The features in the financial data that are used to predict the loan status are loan size, interest rate, borrower income,  debt to income ratio, number of accounts, derogatory marks and total debt. 
* For the target values of <samp>loan_status</samp> there are two variables which I have tried to predict. The first set of variables have a value of '0' (value count of healthy loans = 18759) and these indicate that the loan is healthy. The second set of variables have a value of '1' (value count of unhealthy loans = 625) and these mean that the loan has a high risk of defaulting.

### The machine learning process used to perform the analysis has the following stages: 
1. Create label sets and feature Dataframe from the provided dataset.
2. Split the data into training and testing datasets by using train_test_split.
3. Create a logistic regression model and fit our original data into the model.
4. Make predictions on testing data labels by using the testing feature data and the fitted model.
5. Evaluate the model's performance by calculating accuracy scores, confusion matrix, and classification report.
6. The first method used in this case is the LogisticRegression model on the original fitted data. As the data was highly overweighted towards one of the target variables (healthy loans), therefore, RandomOverSampler was used to reduce the imbalances & LogisticRegression was then applied to the oversampled data.

## Results
Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.

* Machine Learning Model 1 - Original Data - <ins>Logistic Regression</ins>:

The following are key results that can be drawn from the results computed by the Logistic Regression model that was performed on the original fitted data:

<p align="center">
<img src="https://github.com/molleighH/credit-risk-classification/blob/main/Credit_Risk/Resources/original_data_classification_report.png" width="600" height="300" border="10"/>
</p>

* For the original data, the accuracy score is 99%, which reveals that the model has been highly accurate. 
* For the original data, the precision score for health loans is 100%. The precision for high-risk loans is 87%; therefore, the remaining 13% are false-positives. Out of all the loans that the model predicted would be high-risk, only 87% were actually high-risk.
* For the original data, high-risk loans have a recall score is 89%; therefore, the remaining 11% are false negatives. Out of all the loans that actually were high-risk, the model only predicted this outcome correctly for 89% of those high-risk loans. 


  * Machine Learning Model 2 - Oversampled Data - <ins>Logistic Regression</ins>:

<p align="center">
<img src="https://github.com/molleighH/credit-risk-classification/blob/main/Credit_Risk/Resources/oversampled_data_classification_report.png" width="600" height="300" border="10"/>
</p>

  * For the oversampled data, the accuracy score is 100%, which reveals that the model is now even more accurate. 
  * For the oversampled data, the precision for high-risk loans remains 87%; therefore, the remaining 13% are false-positives. Out of all the loans that the model predicted would be high-risk, only 87% were actually high-risk.
  * For the oversampled data, high-risk loans have a recall score is 100%; therefore, their are no false negatives. Out of all the loans that actually were high-risk, the model predicted this outcome correctly for 100% of those high-risk loans. 
  * Additionally, for the oversampled data, the f1-score has increased by 5%, which indicates that the model is now more precise.

## Summary
Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.
 * The Logistic Regression Model created on the original data performed slightly worse than the model created on the oversampled data. As a result, oversampling can be seen as a helpful tool when trying to create a successful model. This model is highly accurate; however, I would not recommend this model, because there is still room for improvement, because the precision score remained the same (at 87%), and as a result, the f1-score may have increased by 5%, but 93% f1-score for the oversampled data has not reached the classic "95%" mark that most companies must meet in order to move forward. 