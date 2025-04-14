# BigDataProject
Big Data Module Project @ ICBS: Predicting Loan Defaults

## Description
The CSV file is not uploadable to GitHub due to its size, but it can be found on kaggle via https://www.kaggle.com/datasets/yasserh/loan-default-dataset/data

This code cleans the data that was presented by filling the missing values (mean fill for numeric, mode fill for other), and handles the outlier data by clipping them using the IQR to determine outliers.

Different models were used to try to predict the defaulting vs non-defaulting rate, including Logit, Decision Trees, and Random Forests.

The Random Forest model was deemed the most optimal in initial testing, which called for further tuning to improve the results.

Improvements included tuning parameters (such as number of estimators, leafs, and more) and finding the optimal model by cross validation through GridSearchCV and RandomizedSearchCV (the latter was used for faster processing in later testing).

The data itself was rebalanced using SMOTE (Synthetic Minority Oversampling Technique), as there was an imbalance between the total number of defaulters and non-defaulters.

The end result was an ROC-AUC of 0.84, and the model deemed that credit_type was the most important feature, followed by income, credit_score, and loan_amount to determine if a loaner is to default or not.

## Conclusion and Summary
### Model Comparison and Performance
- Multiple models were compared during this project, and the random forest was found to perform better than the others.
- SMOTE was used to fix the natural imbalance between defaulting and non-defaulting data points.
- Further tuning to the random forest was carried out using cross-validation

### Potential Improvements
- Further models can be tested
- Futher tuning could be carried out with more parameters
- A data set with more features could be used to create a more robust model

### Final Advice and Takeaway
- The model should be used only to raise account for further inspection, and not for decision making
