# Module 20: Supervised Learning
Cassio Sperb

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* This analysis aims to predict loan status `(healthy or high-risk)` and evaluate the dataset's quality to develop a reliable prediction model using supervised learning. 
* The dataset contains the loan size, intersts rate, borrower income, debit to income, number of accounts, derogatory marks, total debt and loan status. Used the loan status as target variable separeting it from the rest of the data.
* The loan_status variable (`0` for healthy and `1` for high-risk loans) is supported by 56,262 `0`'s and 1,890 `1`'s in the training model.  
* Description of the stages of the machine learning process:
    * Data preparation: reading the dataset from the CSV file;
    * Separated the loan_stauts column as `y` and removed it from the rest of the DataFrame as `X` variable.
    * Split the data into training and testisn datasets by using `train_test_split`
    * Create a Logistic Regression Model with the Original Data
    * Fit a logistic regression model by using the training data (`X_train` and `y_train`).
    * Save the predictions on the testing data labels by using the testing feature data (`X_test`) and the fitted model.
    * Evaluate the model’s performance.
    * Logistic Regression
        *  A supervised learning algorithm used for binary classification.
        * Provided key metrics such as precision, recall, and F1-score to evaluate model performance.

## Results

* Testing classification report:
    * Accuracy: 0.99
    * precision: 1 for `0` vs 0.86 for `1`
    * recall: 1 for `0` vs 0.93 for `1`
            
## Summary

The model have a perfect precision and recall on identifying the healthy loan, but the precision on identifying the high-risk loan has place to improvement, mainly by increasing the database on this category, since the imbalance dataset (610 vs. 18,774 healthy loans) affects the model's ability to generalize.

I wouldn't recommed this model, because, using the current model without improving the dataset could lead to significant business risks, as accurately identifying high-risk loans is critical. The dataset's imbalance and the relatively lower precision for high-risk loans indicate the need for improvement before relying on the model. 
