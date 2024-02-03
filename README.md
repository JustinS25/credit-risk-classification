# credit-risk-classification


## Overview of the Analysis

In the module 20 assignment, we had been taked to evaluate the effectiveness of the linear regression model on a set of data which included healthy and high risk loans. The purpose of this was to see if this was an effective way to predict how accurate the data is at placing the data points into the correct "buckets". The data which was observed was from a csv file. In the csv we were given various info on the loan size, interest rate, borrower detals, etc. What we needed to predict was whether the loan was being accurately predicted as high risk or not. When doing `value_counts` we were able to see that there were far greater `0`s than `1`s. This meant that more healthy loans were predicted over risky ones. Midway through our analysis, we had to continue by evening out the amounts of `0`s and `1`s using `RandomOverSampler`. Once used, we were able to even output the data and instantiate the logistic regression classifier once more to see if the `0` and `1` predictions were as accurate as they were in the initial data. It turned out that the `balanced_accuracy_score` jumped up quite a bit, deeming the oversampled data to be the more accurately predicted data. When using `RandomOverSampler` it was interesting to find that by resampling the X and y data we are able to output a more accurate prediction model.

## Results

* Machine Learning Model 1:
    * Logistic Regression with Original Data
        * balanced accuracy score:
        `0.9520479254722232`
        * confusion matrix:
        `[[18663   102]`
        `[   56   563]]`
        * classification report:
        `precision    recall  f1-score   support`

           `0       1.00      0.99      1.00     18765`
           `1       0.85      0.91      0.88       619`

    `accuracy                           0.99     19384`
   `macro avg       0.92      0.95      0.94     19384`
`weighted avg       0.99      0.99      0.99     19384`



* Machine Learning Model 2:
    * Linear Regression with Resampled Training Data
        * balanced accuracy score::
        `0.9936781215845847`
        * confusion matrix:
        `[[18649   116]`
        `[    4   615]]`
        * classification report:
        `precision    recall  f1-score   support`

           `0       1.00      0.99      1.00     18765`
           `1       0.84      0.99      0.91       619`

    `accuracy                           0.99     19384`
   `macro avg       0.92      0.99      0.95     19384`
`weighted avg       0.99      0.99      0.99     19384`


## Summary

In conclusion, both machine learning models were rather accurate. The balanced accuracy scores as well as their classification reports strongly reflect these findings. The biggest thing to take a look at for me is the balanced accuracy score. For the resampled data, there was over 0.99 accuracy as opposed to the 0.95 accuracy of the original data. Though still strong, the newer model seems to perform best for our needs. Depending on what we want to solve (aka. accurate `0`s or `1`s) I would highly reccomend using the newer model. 



## Citations

- Utilized class activities to serve as a baseline for code. Derived many functions from module 20, days 1 and 2 classwork.

- Used Ask BCS for help with [from imblearn.over_sampling import RandomOverSampler](https://imbalanced-learn.org/stable/over_sampling.html) segment. Provided website with documentation on that portion:
https://imbalanced-learn.org/stable/over_sampling.html