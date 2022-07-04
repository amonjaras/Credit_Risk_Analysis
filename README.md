# **Credit Risk Analysis**
Module 17: Supervised Machine Learning

## **INDEX**

- [Overview](#overview)
- [Resources](#resources)
- [Results](#results)
  - [Resampling Models](#resampling-models)
  - [Ensemble Classifiers](#ensemble-classifiers)
- [Summary](#summary)

## **Overview**

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, we’ll need to employ different techniques to train and evaluate models with unbalanced classes. For this Challenge, Jill asks to use `imbalanced-learn` and `scikit-learn` libraries to build and evaluate models using resampling.

Using the credit card credit dataset from **LendingClub**, a peer-to-peer lending services company, we’ll oversample the data using the `RandomOverSampler` and `SMOTE` algorithms, and undersample the data using the `ClusterCentroids` algorithm. 

Then, we’ll use a combinatorial approach of over- and undersampling using the `SMOTEENN` algorithm. Next, we’ll compare two new machine learning models that reduce bias, `BalancedRandomForestClassifier` and `EasyEnsembleClassifier`, to predict credit risk. 

[:top: Go To Top](#index)

## **Resources**

### **Data**

- [Credit Card Dataset](https://github.com/amonjaras/Credit_Risk_Analysis/blob/main/Module_Challenge/Resources/LoanStats_2019Q1.csv)

### **Tools**

- Jupyter Notebook
- Python

[:top: Go To Top](#index)

## **Results**

### **Resampling models**

✅ **[Deliverable 1 and 2](https://github.com/amonjaras/Credit_Risk_Analysis/blob/main/Module_Challenge/credit_risk_resampling.ipynb)**

#### **Random Oversampling**

> *Fig 1: Oversampling*

![oversampling](https://github.com/amonjaras/Credit_Risk_Analysis/blob/main/images/oversampling.png)

As displayed on Fig 1, below some remarks:

- The accuracy score is around **65%**
- The precision for High_Risk is = **0.01**
- The precision for Low_Risk is = **1**
- The recall for High_Risk is too low = **0.61**
- The recall for Low_Risk is too high = **0.69**

#### **SMOTE Oversampling**

> *Fig 2: SMOTE oversampling*

![smote](https://github.com/amonjaras/Credit_Risk_Analysis/blob/main/images/smote_over.png)

Analysing Fig 2, below some remarks:

- The accuracy score is around **64%**
- The precision for High_Risk is too low = **0.01**
- The precision for Low_Risk is too high = **1**
- The recall for High_Risk is = **0.62**
- The recall for Low_Risk is = **0.65**

#### **Cluster Centroids Undersampling**

> *Fig 3: Undersampling*

![undersampling](https://github.com/amonjaras/Credit_Risk_Analysis/blob/main/images/Undersampling.png)

For Fig 3, we have the following remarks:

- The accuracy score is around **53%**
- The precision for High_Risk is too low = **0.01**
- The precision for Low_Risk is too high = **1**
- The recall for High_Risk is = **0.61**
- The recall for Low_Risk is = **0.45**

#### **SMOTEENN**

> *Fig 4: SMOTEENN*

![smoteenn](https://github.com/amonjaras/Credit_Risk_Analysis/blob/main/images/smoteenn.png)

From Fig 4, we extract the following remarks:

- The accuracy score is around **62%**
- The precision for High_Risk is too low = **0.01**
- The precision for Low_Risk is too high = **1**
- The recall for High_Risk is = **0.70**
- The recall for Low_Risk is = **0.54**

[:top: Go To Top](#index)

### **Ensemble Classifiers**

✅ **[Deliverable 3](https://github.com/amonjaras/Credit_Risk_Analysis/blob/main/Module_Challenge/credit_risk_ensemble.ipynb)**

#### **Balanced Random Forest**

> *Fig 5: Balanced Random Forest*

![brf](https://github.com/amonjaras/Credit_Risk_Analysis/blob/main/images/brf.png)

From Fig 5, we can remark the following:

- The accuracy score is around **78%**
- The precision for High_Risk is = **0.04**
- The precision for Low_Risk is = **1**
- The recall for High_Risk is = **0.67**
- The recall for Low_Risk is = **0.91**

#### **Easy Ensemble Classifier**

> *Fig 6: Easy Ensemble*

![eec](https://github.com/amonjaras/Credit_Risk_Analysis/blob/main/images/eec.png)

After Fig 6, we have the following remarks:

- The accuracy score is around **93%**
- The precision for High_Risk is = **0.07**
- The precision for Low_Risk is = **1**
- The recall for High_Risk is = **0.91**
- The recall for Low_Risk is = **0.94**

[:top: Go To Top](#index)

## **Summary**

After comparing all the results from different ML models, the `EasyEnsembleClassifier` model returned better results with an accuracy of **93%** and **7%** precision rate when predictic "High Risk" candidates.
Looking to the Sensitivity rate (Recall) we noted also a higher value with **91%** comparing with the rest of the models.
It is important to mention that the original dataset had mayority of the applicatios classified as "Low Risk" and minority as "High Risk" category; with this classification the results would be highly affected and there is a risk that the `Machine Learning` algorithms are creting clusters from too small datasets of "High Risk" applications.

[:top: Go To Top](#index)



This work belongs to [^1].
Course [^2].
[^note]:
[^1]: Author: Audrey MONJARAS :mexico: :panama: :canada:
[^2]: Data Analytics: Unit 17 SML
