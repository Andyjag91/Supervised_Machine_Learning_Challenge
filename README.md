# Supervised_Machine_Learning_Challenge
##  Predicting Credit Risk

## Objective
To build a machine learning model that attempts to predict whether a loan from LendingClub will become high risk or not. 

## Background

LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.

 Data was used to create machine learning models to classify the risk level of given loans. Specifically, comparing the Logistic Regression model and Random Forest Classifier.

## Procedure
- Retrieve the data (in CSV format) show below:
  * `2019loans.csv`
  * `2020Q1loans.csv`

The CSVs contain an entire year's worth of data (2019) to predict the credit risk of loans from the first quarter of the next year (2020).

*these two CSVs have been undersampled to give an even number of high risk and low risk loans. In the original dataset, only 2.2% of loans are categorized as high risk. To get a truly accurate model, special techniques need to be used on imbalanced data. Undersampling is one of those techniques. Oversampling and SMOTE (Synthetic Minority Over-sampling Technique) are other techniques that are also used.

## Preprocessing: Convert categorical data to numeric

A training set was created from the 2019 loans using `pd.get_dummies()` to convert the categorical data to numeric columns. Similarly, a testing set was created from the 2020 loans, also using `pd.get_dummies()`. There are categories in the 2019 loans that do not exist in the testing set. If a model was fitted to the training set scored on the testing set as is, an error will occur. Coding will need to be used to fill in the missing categories in the testing set. 

## Considering the models

Two models will be created and compared on this data: a logistic regression, and a random forests classifier. 

Before created, fit, and score the models, a prediction was made as to which model will perform better.

## Fitting a LogisticRegression model and RandomForestClassifier model

A LogisticRegression model was created, fitted to the data, and scored based on the models performance. The same was done for a RandomForestClassifier.

## Revisit the Preprocessing: Scaling of data
The data going into these models was never scaled, an important step in preprocessing. The functionm `StandardScaler` was used to scale the training and testing sets.

The LogisticRegression and RandomForestClassifier models were Fit and scored on the scaled data. 

### Results:
- 
- Logistic Regression is a better model fit for the data and is also sensitive when the data is scaled and when important features are selected. For Random Forest there is no visible change once the data is scaled and improtant features are selected.

### Conclusion 

- Logistic Regression is a better model fit for the data and is also sensitive when the data is scaled and when important features are selected. For Random Forest there is no visible change once the data is scaled and improtant features are selected.
### References

LendingClub (2019-2020) _Loan Stats_. Retrieved from: [https://resources.lendingclub.com/](https://resources.lendingclub.com/)
