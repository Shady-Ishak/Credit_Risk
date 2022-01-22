# Credit_Risk_Analysis

Credit Risk Analysis Project Overview:
---

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans.

Using a credit card credit dataset and Python, several machine learning modules will be used to evaluate and predict credit risk.

Once these models have been completed, their performance will be evaluated and a written recommendation will be made on whether they should be used to predict credit risk


Technical used in this project to predict credit risk:
---

Oversample the data using the RandomOverSampler and SMOTE algorithms.
Undersample the data using the ClusterCentroids algorithm.
A combinatorial approach of over- and undersampling using the SMOTEENN algorithm.
Compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk.

Deliverables:
---

Deliverable 1: Use Resampling Models to Predict Credit Risk
Deliverable 2: Use the SMOTEENN Algorithm to Predict Credit Risk
Deliverable 3: Use Ensemble Classifiers to Predict Credit Risk
Deliverable 4: A Written Report on the Credit Risk Analysis

# Deliverable 1 Results: Use Resampling Models to Predict Credit Risk
---
Oversampling RandomOverSampler Model:
---

1)randomoversampler_balanced_accuracy
2)randomoversampler_confusion_matrix
3)randomoversampler_classification_report

Accuracy Score for the RandomOverSampler model is 63%
The precision for the high-risk is 1% and F1 score is 2%, which are not good enough to state that the model will be good at classifying.

SMOTE Oversampling Model:
---

1)smote_balanced_accuracy
2)randomoversampler_confusion_matrix
3)randomoversampler_classification_report

The accuracy score of the SMOTE model is a little bit better than the RandomOverSampler.
The precision for the high-risk is very low at 1%, indicating a large number of false positives, which indicates an unreliable classification.
The F1 score is 2% which also very low.

Undersampling ClusterCentroids Model:
---

The 51% accuracy score of ClusterCentroids model performs poorly when compared to the RandomOverSampler and SMOTE models.
The precision (1%) and the F1 (1%) are still very low just like the RandomOverSampler and SMOTE models.
The ClusterCentroids model is not good at classifying fraudulent loan applications because the model's accuracy, 0.516, and F1 score are low.

# Deliverable 2 Results: Use the SMOTEENN Algorithm to Predict Credit Risk
---

Combination Sampling SMOTEENN Model:
---

We do see an increase accuracy score (63%) over the ClusterCentroids model (51%) but still about same as RandomOverSampler and SMOTE models accuracy scores.
The precision (1%) and the F1 (1%) are still very low for high-risk group, just like the RandomOverSampler, SMOTE and Clustercentroids models.

# Deliverable 3 Results: Use Ensemble Classifiers to Predict Credit Risk
---

Balanced Random Forest Classifier Model:
---

1)The precision score for the high-risk has improved a bit (4%), but still indicates a large number of false positives, which indicates an unreliable positive classification.
2)The F1 score is still low (14) but improving.

Easy Ensemble AdaBoost Classifier Model:
---

The accuracy score of the EasyEnsembleClassifier model is a much improved 93% over all the other models.
The high-risk precision (7) and F1 score (14) have improved over all the other models.
The low-risk precision (1.0) and recall (94) and F1 (97) are the highest of all the models.


Credit Risk Analysis Project Summary:
---
Overview of the analysis: Explain the purpose of this analysis.

After creating and evaluating these machine learning models it's easy to see that all the models show poor precision when it comes to predicting if a credit risk is high.

It wasn't until the Ensemble models (Easy Ensemble AdaBoost Classifier especially) were used that there was an improvement in accuracy scores. The EasyEnsembleClassifier model did show strong recall for both high-risk(91%) and low-risk(94%).

Key takeaways from Predicting Credit Risk Project:

The performance of all the models showed very poor precision for accessing if a credit risk is high.
A majority of the models had accuracy score ranging between 51% - 65%
The Balanced Random Forest Classifier and Easy Ensemble
I would not recommend any use of these models to predict credit risk. Using these models could lead LendingClub to reject high-risk individuals when, in fact, they are low-risk..
