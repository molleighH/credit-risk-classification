# Credit Risk Classification
## Overview of the Analysis 
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

## Results : Using a bulleted list, describe the accuracy score, the precision score, and recall score of the machine learning model.

<p align="center">
<img src="https://github.com/molleighH/credit-risk-classification/blob/main/Credit_Risk/Resources/original_data_classification_report.png" width="400" height="300" border="10"/>
</p>



3. <ins>A summary:</ins> Summarize the results from the machine learning model. Include your justification for recommending the model for use by the company. If you don’t recommend the model, justify your reasoning.

