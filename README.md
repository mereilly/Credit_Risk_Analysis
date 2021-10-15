# Credit_Risk_Analysis

## Overview of the Analysis: 
#### background of project

Working with FastLending, we wanted toestablish an accurate selector, for a quick and reliable model for predicting credit risk candidates for loans to lower default rates. Working with Jill, the lead data scientist on this project, I used a carefully selected classification, supervised Machine Learning Model (ML model) on prepared data to which to apply statistical reasoning.

#### purpose of this analysis
The purpose is mainly to establish which ML model is better at predicting credit risk through resampling and combinatorial approaches, sampling six ML models.

## Results of Six Machine Learning Models:
#### the balanced accuracy scores (xx.xx%) :
    - Naive RandomOversampler : 60.28%
    - SMOTE Oversampling : 60.28%
    - ClusterCentroids Resampler: 63.29%
    - Logistical Regression SMOTEENN : 49.82%
    - Random Forest Classifier : 82.29%
    - EasyEnsemble AdaBoost Classifier : 94.56%

#### the precision score (as derived from the classification_report)
    - Naive RandomOversampler : 0.01
    - SMOTE Oversampling : .01
    - ClusterCentroids Resampler : .01
    - Logistical Regression SMOTEENN  : .00
    - Random Forest Classifier : 0.03 
    - EasyEnsemble AdaBoost Classifier  :  0.07

##### recall score (as derived from the classification_report)
    - Naive RandomOversampler : .57
    - SMOTE Oversampling : .57
    - ClusterCentroids Resampler : .62
    - Logistical Regression SMOTEENN  : .51
    - Random Forest Classifier : .74
    - EasyEnsemble AdaBoost Classifier  : .94

Classification reports for 

the ClusterCentroids Resampler 

and  EasyEnsemble AdaBoost Classifier :  

## Summary: 
When comparing just the scores from the resampling excercised rounded to the 100th decimal place, we can see the th ClusterCentroids Resampler method proves to be most effective by a narrow margin. But when we include the ensempble classifiers for the same consideration, there is no question the EasyEnsemble AdaBoost Classifier is far superior with about 95% accuracy and .94 recall. Thus, I would recommend we focus future efforts using thie EasyEnsemble AdaBoost Classifier  even if the initial tasks take a little longer, the objective was to craft RELIABLE predictions, a parameter that is prioritized above speed then. But, it didn't take too much longer in our simulations regardless.

