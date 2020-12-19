# Credit_Risk_Analysis

## Overview

In this assignment , Python was used to build and evaluate several machine learning models to determine and predict credit risk.

The following method was adopted:

- Oversample data using RandomOverSampler and SMOTE algorithm
- Undersample data using ClusterCentroids algorithm
- Use combinatorial approach of under and over sampling with SMOTEENN algorithm
- Compare two machine learning models to reduce bias (EasyEnsembleClassifier & BalanceRandomForestClassifier)


The performance of these models were used to make a recommendation on whether it should be used to predict credit risk.

## Results 
Balanced Accuracy Scores, Confusion Matrixes and Imbalanced Classification Reports

## RandomOverSampler Model
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/Classification%20Report.png>
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/BalancedAccuracy.png>

The balanced accuracy score is 65%.
The high_risk precision is about 1% only with 61% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 68%.


## SMOTE Model
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/SMOTE.png>
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/SMOTE1.png>

The results are pretty similar to the previous model.
The balanced accuracy score is 65%.
The high_risk precision is about 1% only with 64% sensitivity which makes a F1 of 2% only.
Due to the high number of the low_risk population, its precision is almost 100% with a sensitivity of 67%.

## ClusterCentroids Model
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/ClusterModel.png>
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/ClusterModel1.png>

Here the balanced accuracy score is down to about 51%.
The high_risk precision is still 1% only with 63% sensitivity which makes a F1 of 1%.
Due to the high number of false positives, the low_risk sensitivity is only 40%.

## SMOTEENN Model
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/Smoteenn%20Model.png>
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/Smoteenn%20Model1%20.png>

The balanced accuracy score is about 64%.
The high_risk precision is still 1% only with 70% sensitivity which makes a F1 of only 2%.
Due to the high number of false positives, the low_risk sensitivity is 57%.

## BalancedRandomForestClassifier Model
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/BalanceRandomForest%201.png>
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/BalanceRandomForest%202.png>
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/BalanceRandomForest%203.png>

The balanced accuracy score improved to about 79%.
The high_risk precision is still low at 4% only with 67% sensitivity which makes a F1 of only 7%.
Due to a lower number of false positives, the low_risk sensitivity is now 91% with 100% presicion.


## EasyEnsembleClassifier Model
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/EasyEnsembleClassifier1.png>
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/EasyEnsembleClassifier2.png>
<img src= https://github.com/uferdousi197/Credit_Risk_Analysis/blob/main/EasyEnsembleClassifier3.png>

Now, the balanced accuracy score is high to about 93%.
The high_risk precision is still low at 7% only with 91% sensitivity which makes a F1 of only 14%.
Due to a lower number of false positives, the low_risk sensitivity is now 94% with 100% presicion.

## Summary
The models above used to perform the credit risk analysis shows weak precision in determining if the credit risk is high. 
The Ensemble model shows a lot of improvment on the sensitivity of the high risk credit. 
The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. 
However, with a low precision, a lot of low risk credits are still falsely detected as high risk 
which would make the bank's credit strategy poor and infer on its revenue by missing business opportunities. 
Therefore, I would not recommend the bank to use any of these models to predict credit risk.



