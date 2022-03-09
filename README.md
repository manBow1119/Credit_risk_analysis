# Credit_risk_analysis

### Project Overview
The purpose of this analysis was to use peer-to-peer lending data to determine which Machine Learning sampling and classifying models showed the best performance for predicting credit risk for credit card applications. The SMOTE and RandomOverSample oversampling algorithms were fit and tested, while ClusterCentroids algorithm was used for an undersampling approach. Combining both approaches, the SMOTEEENN algorithm was also tested. Finally, to reduce bias ensemble approaches including the BalancedRandomForestClassifier and EasyEnsembleClassifier models were also fit and tested. Balanced accuracy scores, cofusion matrices, and classification reports were all examined to determine the fitness of each model in this context.

### Technologies/Libraries
* Python, Jupyter Notebooks
* pandas, numpy, sklearn, imblearn, matplotlib

### Results of each model
* RandomOverSample
  * Balanced Accuracy Score: 0.633
  * Precision, Recall: 0.99, 0.63
  * F1: 0.77

* SMOTE
  * Balanced Accuracy Score: 0.664
  * Precision, Recall: 0.99, 0.66
  * F1: 0.79

* ClusterCentroids
  * Balanced Accuracy Score: 0.664
  * Precision, Recall: 0.99, 0.45
  * F1: 0.62

* SMOTEENN
  * Balanced Accuracy Score: 0.641
  * Precision, Recall: 0.99, 0.59
  * F1: 0.74

* BalancedRandomForestClassifier
  * Balanced Accuracy Score: 0.789
  * Precision, Recall: 0.99, 0.87
  * F1: 0.93

* EasyEnsembleClassifier
  * Balanced Accuracy Score: 0.915
  * Precision, Recall: 0.99, 0.90
  * F1: 0.94

### Summary of Results
The statistical metrics used to determine the fitness of each model for predicting credit risk allow for quick analytical comparison. In paricular, the Balanced Accuracy of each model shows a distinct variance between the different approaches. Basic oversampling returned the lowest accuracy scores, with SMOTE only slightly improving on accuracy and F1 scores. Basic undersampling (ClusterCentroids) returned the lowest recall, and resulting F1 scores. Interestingly, the combined SMOTEEN algorithm did not show considerable improvement on either basic sampling algorithm it combines. When the ensemble classifiers were employed, we can see the benefit of this algorithmic approach. By reducing spread and improving predictive performance of each ensemble member, the overall combination of these simpler models provides more accuracy and robustness of predictions. The EasyEnsembleClassifier certainly had the highest accuracy score; high precision and recall score yielded the highest F1 of all models as well. While none of these models achieves near perfection in prdeicting credit risk, the EasyEnsembleClassifier certainly proved to perform the best for this context, with a predictive accuracy of 91.5%. Depending on the desired threshold for accuracy, this model has potential to be quite useful. 
