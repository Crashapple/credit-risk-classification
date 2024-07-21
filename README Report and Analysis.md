# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to use various techniques to train and evaluate a model based on loan risk. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers. 

* The dataset, lending_data.csv, contains financial information about various loans, including:

    * loan_size: The amount of the loan.
    * interest_rate: The interest rate charged on the loan.
    * borrower_income: The borrower's annual income.
    * debt_to_income: The ratio of the borrower's total debt to their income.
    * num_of_accounts: The number of accounts the borrower has.
    * derogatory_marks: The number of derogatory marks on the borrower's credit report.
    * total_debt: The total debt owed by the borrower.
    * loan_status: The target variable, indicating whether the loan is healthy (0) or high risk (1).

* The stages of machine learning were:

    * Read the lending data from the provided csv file into a Pandas DataFrame.
    * Create the labels set (`y`)  from the “loan_status” column, and then create the features (`X`) DataFrame from the remaining columns.
    * Split the data into training and testing datasets by using `train_test_split`.
    * Fit a logistic regression model by using the training data (`X_train` and `y_train`).
    * Save the predictions on the testing data labels by using the testing feature data (`X_test`) and the fitted model.
    * Evaluate the model’s performance by:
        * Generate a confusion matrix.
        * Print the classification report.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1: Logistic Regression
    * Accuracy: 0.99
        * This indicated the model accurately predicted the loan status of 99% of the test data.
    * Precision: Class 0 - 1.00; Class 1 - 0.85
        * The Precision for Class 0 is 100%, meaning there were no false positives for this test data.
        * The Precision for Class 1 indicated that 85% of the loans that were predicted to default, truly defaulted.
    * Recall: Class 0 - 0.99; Class 1 - 0.91
        * The Recall for Class 0 indicates that 99% of the loans predicted to not default, did not in fact default.
        * The Recall for Class 1 indicated that 91% of the loans predicted to default, did in fact default.

## Summary

Only the Logistic Regression model was used in this analysis to predict loan status based on our data. Looking at the high accuracy score of 99% indicates that this is a good model to use for our predictions. 

The performance of predicting loans that would default will be more useful, as that would indicate financial losses. 

