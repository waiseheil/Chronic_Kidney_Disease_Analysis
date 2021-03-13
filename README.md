# Chronic_Kidney_Disease_Analysis

In this work the Chronic Kidney Disease (CKD) dataset from UCI Machine Learning repository has been used to understand how different biological markers get modified when developing CKD and to build two models to predict whether someone has CKD or not. For the former we have found that older people seem to be more prone to develop it and hypertension is a prevalent marker in such cases. For the latter, the features with the most predictive power were found to be, among others, hemoglobin, glucose levels or hypertension. The models show great potential but, as we will discuss, a more extensive dataset is needed for a reliable accuracy measure.

## Motivation

Chronic Kidney Disease (CKD) is characterized by having damaged kidneys that drastically reduces these organ’s filtering power. It affects approximately 9% of the world population. Kidneys do not have the ability to heal themselves and thus, it makes CKD a very dangerous condition. 
It is thus very important for the **non-medical population** to be able to identify how particular markers get modified in the case someone develops CKD: **an early diagnosis improves the prognosis**. Conversely, **medically trained** individuals should have the means to rapidly and effectively detect if someone has CKD and to know what markers are the most important ones to predict this disease.
For these reasons I will (i) delve into how the features that can be **measured at home** by an average person are compared between healthy and sick individuals and (ii) build a classification model to check the dataset potential for diagnosis

# Dataset

Data can be downloaded directly from the dataset folder in this repository or from the [UCI Machine Learning source repository](https://archive.ics.uci.edu/ml/datasets/chronic_kidney_disease). The dataset contains 400 instances and 25 features linked to a binary target label that defines whether someone has CKD or not. 11 features are numerical and 14 nominal. The dataset is imbalanced, that is, it has 250 negative (healthy) and 150 positive (CKD) instances.
When dropping rows with missing values, the number of instances goes down to 114 negatives (healthy) and 43 positives (CKD).
Some of the relevant features are: age, blood pressure, appetite, blood glucose, hemoglobin, ion blood concentration (Sodium and Potassium), among others. 
 
# Research questions

1. How do the following markers behave when someone has CKD?:

   - Age
   - Diastolic blood pressure and hypertension
   - Appetite
   - Blood glucose and diabetes

2. How well can we predict if someone has CKD with Decision Trees and Logistic Regression? What are the most relevant features for the models to make this prediction?

**Important note:** this work does not delve into correlation-causality relation of CKD and the corresponding health markers. Abnormal values of the studied markers must be always consulted with a doctor for a correct assessment, as they may not be a consequence of an already developed CKD. 

## Data treatment, exploration and model building:

For details on data treatment and/or model interpretation/building please read the [analysis summary](./Analysis_Summary.pdf) and the [Jupyter notebook](./Chronic_Kidney_Disease_Project_course.ipynb). 

## Conclusions

1. Health markers exploration for home measurements:
   - CKD has a larger prevalence in people between 40-80 years old
   - Hypertension is a common signal of CKD (80% of sick patients)
   - High glucose levels and diabetes are directly linked with CKD
   - 45% of people with CKD show a poor appetite 

2. Machine learning modelling:
   - Model prediction shows great potential with both decision trees and logistic regression. Logistic regression seems to yield better performance but a larger dataset is needed to correctly assess the model’s real efficiency and accuracy. Note that, since this is an imbalanced dataset, accuracy should not be taken as the only measure of prediction, but also precision and recall, as explicitely noted in the [analysis summary](./Analysis_Summary.pdf).
   - Features with the most predictive power were found to be: 
     - Hemoglobin
     - Hypertension
     - Blood glucose
     - Packed cell volume
     - Creatinine levels
     - Albumin levels
     - Specific gravity











