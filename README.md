# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis:

  The purpose of the loan prediction risk analysis was to build a supervised machine learning model that will be helpful in predicting credit risk. The target variable for our model is the loan-status, which we have preprocessed to contain "high-risk" or "low-risk" classes. These classes are unbalanced because low-risk loans outnumber high-risk loans, so we are using some algorithms from the imbalanced-learn library. First we used Oversampling with RandomOverSampler and SMOTE, then Undersampling with ClusterCentroids, then a combined approach with SMOTEENN and finally BalancedRandomForestClassifier and EasyEsembleClassifier. Our goal was to see which model is the most helpful in predicting risk so Jill can pitch to potential investors.

## Describe the balanced accuracy score and the precision and recall scores of all six machine learning models:

- RandomOverSampler - 0.9941296134844522
- SMOTE - 0.6420277463901676
- RandomUnderSampler - 0.6420277463901676
- SMOTEENN - 0.5794568348322204
- BalancedRandomForestClassifier - 0.9996784377923293
- EasyEnsembleClassifier - 1.0

Recommendation on which model to use, (or there is no recommendation with a justification):
