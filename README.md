# Credit_Risk_Analysis


Credit Risk Analysis
Overview
In this analysis I test the successfulness of several machine learning models to at predicting the risk status of loans based on a large number of criteria from LendingClub's credit card dataset.

Results
Displayed below are the balanced accuracy, precision, and recall for each model where a high risk loan ('1') is defined as a true positive result. Below these are the classification reports generated throught the Imbalanced Learn library.

Note that, in these contexts, precision represents the number of high risk loans correctly identified divided by the total number of high risk loans identified (true and false positives). Recall represents the number of high risk loans correctly identified divided by the total number of true high risk loans. The balanced accuracy is the mean of the percentages of true high risk loans and true low risk loans identified by the model. (See: https://en.wikipedia.org/wiki/Precision_and_recall).

Model 1: Naive Random Oversampling
precision: .01
recall : .57
balanced accuracy: .61
                pre       rec       spe        f1       geo       iba       sup
    0          1.00      0.66      0.57      0.79      0.61      0.38     13711
    1          0.01      0.57      0.66      0.01      0.61      0.37        53
avg / total    0.99      0.66      0.57      0.79      0.61      0.38     13764
Model 2: SMOTE Oversampling
precision: .01
recall: .64
balanced accuracy: .64
                pre       rec       spe        f1       geo       iba       sup
    0          1.00      0.65      0.64      0.78      0.64      0.41     13711
    1          0.01      0.64      0.65      0.01      0.64      0.41        53
avg / total    0.99      0.65      0.64      0.78      0.64      0.41     13764
Model 3: Cluster Centroids Undersampling
precision: .00
recall: .51
balanced accuracy: .50
                pre       rec       spe        f1       geo       iba       sup
    0          1.00      0.49      0.51      0.65      0.50      0.25     13711
    1          0.00      0.51      0.49      0.01      0.50      0.25        53
avg / total    0.99      0.49      0.51      0.65      0.50      0.25     13764
Model 4: SMOTEEN
precision: .01
recall: .77
balanced accuracy: .67
                pre       rec       spe        f1       geo       iba       sup
   0           1.00      0.56      0.77      0.72      0.66      0.43     13711
   1           0.01      0.77      0.56      0.01      0.66      0.44        53
avg / total    0.99      0.56      0.77      0.72      0.66      0.43     13764

Model 5: Balanced Random Forest
precision: .03
recall: .60
balanced accuracy: .76
               pre       rec       spe        f1       geo       iba       sup
   0          1.00      0.92      0.60      0.96      0.74      0.57     13711
   1          0.03      0.60      0.92      0.05      0.74      0.54        53
avg / total   0.99      0.91      0.60      0.95      0.74      0.57     13764
Model 6: Easy Ensemble AdaBoost
precision: .07
recall: .94
balanced accuracy: .95
              pre       rec       spe        f1       geo       iba       sup
   0         1.00      0.95      0.94      0.97      0.95      0.89     13711
   1         0.07      0.94      0.95      0.12      0.95      0.89        53
avg / total  1.00      0.95      0.94      0.97      0.95      0.89     13764
Summary
Considering the above models, I would suggest using Model 6: Easy Ensemble AdaBoost. In the context of this application, identifying the relatively small number of high risk loans amongst the many low risk loans seems to be the most important factor in evaluating these models. Therefore, I think this is the best of the models tested because it surpasses the other models in all three metrics measured, and, most importantly, it has a much higher recall rate than any of the other models, meaning it identified more high risk loans correctly than any of the other models.