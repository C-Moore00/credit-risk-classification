# Module 12 Report Template

## Overview of the Analysis
The purpose of this analysis is to create a regression model capable of predicting whether a loan will be accepted or denied based on various inputs.

Provided, we received:
loan_size - The size of the Loan.
interest_rate - the Interest Rate in % of the loan.
borrower_income - the borrower's income per year.
debt_to_income - The Borrower's debt-income ratio as a %.
num_of_accounts - The number of accounts the borrower possesses.
derogatory_marks - the derogatory marks they posses. (Note - I am not quite sure what this is!)
total_debt - The total debt currently incurred by the borrower.

Finally, we received loan_status - Whether a loan was accepted or declined.

loan_status is the variable we wish to predict. All other variables are inputs or X-values.

To investigate this, we performed a created a simple logistical regression model, and trained it on a training subset of the data, consisting of ~58k records of our total ~78k.

## Results

The results of the regression were as follows:

Confusion matrix
------------------

Predicted / Real
      pos     neg
pos   18679    80
neg   67      558

Stats
------------------
- Accuracy: 99.24%
- Precision: 99.67%
- Recall: 99.64%


## Summary
In a brief summary - This model turns out to be remarkably accurate, given the myriad of inputs it takes in.

However, I fear that it may have overfit the existing data. Though the sample is quite large, without trial on another set of loan data, I question if the model is truly functional.

Without another to test, we cannot take the astonishing accuracy, precision and recall at face value.

Additionally, the model was far more likely to give a false negative than a false positive - With the comparative number of negatives and positives, only a mere 67 of the 625 accepted loans were inaccurately predicted.