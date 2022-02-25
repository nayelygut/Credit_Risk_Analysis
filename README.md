# Credit_Risk_Analysis

## Overview of the analysis: 
In this analysis, I used machine learning to look at credit card risk. The credit card dataset comes from LendingClub, a peer-to-peer lending services company. Six different algorithms were used analyzed to decide which one would perform best at predicting credit card risk. 

## Results: describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

-  Oversampling algorithms

    - Naive random oversampling algorithm 
        Balanced Accuracy Score: 0.6547385707934685
        Classification Report Imbalanced:
                        pre       rec       spe        f1       geo       iba       sup

        high_risk       0.01      0.72      0.59      0.02      0.65      0.43       101
        low_risk        1.00      0.59      0.72      0.74      0.65      0.42     17104
        avg / total     0.99      0.59      0.72      0.73      0.65      0.42     17205

    SMOTE algorithm
        Balanced Accuracy Score: 0.66201409663885
        Classification Report Imbalanced:
                        pre       rec       spe        f1       geo       iba       sup

        high_risk       0.01      0.63      0.69      0.02      0.66      0.43       101
        low_risk        1.00      0.69      0.63      0.82      0.66      0.44     17104
        avg / total     0.99      0.69      0.63      0.81      0.66      0.44     17205

-  Undersampling algorithms

    ClusterCentroids to resample data
        Balanced Accuracy Score: 0.5447339051023905
        Classification Report Imbalanced:
                        pre       rec       spe        f1       geo       iba       sup
        high_risk       0.01      0.69      0.40      0.01      0.52      0.28       101
        low_risk        1.00      0.40      0.69      0.57      0.52      0.27     17104
        avg / total     0.99      0.40      0.69      0.56      0.52      0.27     17205

-  Combination algorithms

    SMOTEENN Algorithm
        Balanced Accuracy Score: 0.5447339051023905
        Classification Report Imbalanced:
                        pre       rec       spe        f1       geo       iba       sup

        high_risk       0.01      0.71      0.57      0.02      0.64      0.41       101
        low_risk        1.00      0.57      0.71      0.73      0.64      0.40     17104
        avg / total     0.99      0.57      0.71      0.72      0.64      0.40     17205

-  Ensemble learners

    Balanced Random Forest Classifier
        Balanced Accuracy Score: 0.7887512850910909
        Classification Report Imbalanced:
                        pre       rec       spe        f1       geo       iba       sup

        high_risk       0.03      0.70      0.87      0.06      0.78      0.60       101
        low_risk        1.00      0.87      0.70      0.93      0.78      0.63     17104
        avg / total     0.99      0.87      0.70      0.93      0.78      0.63     17205
    
    Easy Ensemble AdaBoost Classifier
        Balanced Accuracy Score: 0.931601605553446
        Classification Report Imbalanced:
                        pre       rec       spe        f1       geo       iba       sup

        high_risk       0.09      0.92      0.94      0.16      0.93      0.87       101
        low_risk        1.00      0.94      0.92      0.97      0.93      0.87     17104
        avg / total     0.99      0.94      0.92      0.97      0.93      0.87     17205


## Summary: 

- The oversampling, undersampling, and combined algorithms all had the same precision score. 
- The top performing algorithms for this dataset were the 2 ensemble learners: Balanced Random Forest Classifier and Easy Ensemble AdaBoost Classifier. 
- I recommend using the Easy Ensemble AdaBoost Classifier since it had the highest accuracy score, as well as the highest precision and recall scores. 