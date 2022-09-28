# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis:

  The purpose of the loan prediction risk analysis was to build a supervised machine learning model that will be helpful in predicting credit risk. The target variable for our model is the loan-status, which we have preprocessed to contain "high-risk" or "low-risk" classes. These classes are unbalanced because low-risk loans outnumber high-risk loans, so we are using some algorithms from the imbalanced-learn library. First we used Oversampling with RandomOverSampler and SMOTE, then Undersampling with ClusterCentroids, then a combined approach with SMOTEENN and finally BalancedRandomForestClassifier and EasyEsembleClassifier. Our goal was to see which model is the most helpful in predicting risk so Jill can pitch to potential investors.

## Describe the balanced accuracy score and the precision and recall scores of all six machine learning models:

- Accurary Score: 
Assess a model with discrete outcomes. not always an appropriate or a meaningful performance metric, however.
- Precision: 
Also known as positive predictive value (PPV), is a measure of this. Precision is obtained by dividing the number of true positives (TP) by the number of all positives (i.e., the sum of true positives and false positives, or TP + FP). Precision = TP/(TP + FP)
- Recall: 
How likely is it that the test will diagnose it? Sensitivity = TP/(TP + FN)

_______________________________________________________________________________________________________________________________________________________________________
## Algorithms

- RandomOverSampler 
  - Accuracy Score: 
  - Precision: 
  - Recall: 

!()[]

- SMOTE

  - Accuracy Score: 
  - Precision: 
  - Recall: 

!()[]

- RandomUnderSampler 

  - Accuracy Score: 
  - Precision: 
  - Recall: 

!()[]

- SMOTEENN 

  - Accuracy Score: 
  - Precision: 
  - Recall: 

!()[]

- BalancedRandomForestClassifier 

  - Accuracy Score: 
  - Precision: 
  - Recall: 

!()[]

- EasyEnsembleClassifier 


  - Accuracy Score: 
  - Precision: 
  - Recall: 

!()[]

## Recommendation on which model to use, (or there is no recommendation with a justification):
