# Credit_Risk_Analysis

## Overview of the loan prediction risk analysis:

  The purpose of the loan prediction risk analysis was to build a supervised machine learning model that will be helpful in predicting credit risk. The target variable for our model is the loan-status, which we have preprocessed to contain "high-risk" or "low-risk" classes. These classes are unbalanced because low-risk loans outnumber high-risk loans, so we are using some algorithms from the imbalanced-learn library. First we used Oversampling with RandomOverSampler and SMOTE, then Undersampling with ClusterCentroids, then a combined approach with SMOTEENN and finally BalancedRandomForestClassifier and EasyEsembleClassifier. Our goal was to see which model is the most helpful in predicting risk so Jill can pitch to potential investors.

## Describe the balanced accuracy score and the precision and recall scores of all six machine learning models:

- Accurary Score: 
  - Assess a model with discrete outcomes. not always an appropriate or a meaningful performance metric, however.
- Precision: 
  - Also known as positive predictive value (PPV), is a measure of this. Precision is obtained by dividing the number of true positives (TP) by the number of all positives (i.e., the sum of true positives and false positives, or TP + FP). Precision = TP/(TP + FP)
- Recall: 
  - How likely is it that the test will diagnose it? Sensitivity = TP/(TP + FN)

![](https://github.com/jmalauss/Credit_Risk_Analysis/blob/main/Resources/Binary_Outcomes_Table.png)

_______________________________________________________________________________________________________________________________________________________________________
## Algorithms

- RandomOverSampler

This algorithm's performance is accurate according to the accuracy of approximately 99.4%. In other words, the model may result in a small difference between the test and training variables. Given the amount of low-risk loans, the model is more precise in predicting low-risk loans versus high-risk loans according to the precision score in the classification report. It is very likely that the model will predict low-risk loans, and less likely that it will predict high-risk loans.

![RandomOverSampler](https://github.com/jmalauss/Credit_Risk_Analysis/blob/main/Resources/RandomOverSampler.png)

- SMOTE

The accuracy score indicates that the SMOTE algorithm may result in a model that is less accurate at approximately 64.2%. This model is much better at predicting low-risk loans in terms of precision, and poor at high-risk loans. For both low and high-risk loans, it is about the same likeliness that the prediction is correct: 61% and 67%. 

![SMOTE](https://github.com/jmalauss/Credit_Risk_Analysis/blob/main/Resources/SMOTE.png)

- RandomUnderSampler 

This model is accurate 64.2% of the time. It is also precise in predicting low-risk loans, similar to the two models above. There is a minor difference between the sensitivity of the low and high-risk loans predicted by this model, neither are very strong indicators of a high-performing model.

![RandomUnderSampler](https://github.com/jmalauss/Credit_Risk_Analysis/blob/main/Resources/RandomUnderSampler.png)

- SMOTEENN 

This model is accurate about 57.9% of the time. Also very precise in predictions about low-risk loans. Although, this model may be more likely to predict high-risk loans than the models preceeding it.

![SMOTEENN](https://github.com/jmalauss/Credit_Risk_Analysis/blob/main/Resources/SMOTEENN.png)

- BalancedRandomForestClassifier

The accuracy score tells us that the model is accurate about 99.9% of the time. Since this may not be useful, we can look at the other metrics to determine the efficacy of this model. This model is the most precise in low and high-risk loan predictions. So far, our most helpful model.

![BalancedRandomForestClassifier](https://github.com/jmalauss/Credit_Risk_Analysis/blob/main/Resources/BalancedRandomForestClassifier.png)

- EasyEnsembleClassifier 

This model has a perfect accuracy score, precision and recall scores. If there are no errors in the code, this is our best model.

![EasyEnsembleClassifier](https://github.com/jmalauss/Credit_Risk_Analysis/blob/main/Resources/EasyEnsembleClassifier.png)

## Recommendation on which model to use, (or there is no recommendation with a justification):

After completing the analysis, it seems that EasyEnsembleClassifier is the best algorithm to use for our model. We are trying to ask: How good is each model at predicting credit risk? When we take a look at the confusion matrix, we can see that there were 101 correct predictions for high-risk loans, and 17,104 correct predictions of low-risk credit loans. According to the metrics, there were zero errors in prediction from this model. The reason may be that the model was trained and then evaluated. After the model evaluates, it pays more attention to the incorrect predictions to correct them for further training. We can assume the model performed enough time to eliminate the incorrect predictions. This may also mean that the model has enough or good quality data to use for training.
