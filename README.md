# -Survival-Prediction-on-the-Titanic-A-Comparative-Analysis-Using-Machine-Learning-Models-in-R-

[Introduction](#Introduction)

[Aim and Objectives](#aim-and-objectives)

[Data](#data)

[Methodology](#methodology)

[Visualization](#visualization)

[Results and discussion](#results-and-discussion)

[Counclusion and Summary](#counclusion-and-summary)


## Introduction

The sinking of the RMS Titanic in April 1912 remains one of the most infamous maritime disasters in history. Out of the approximately 2,224 passengers and crew members aboard, more than 1,500 lost their lives when the ship struck an iceberg during its maiden voyage from Southampton to New York City (Encyclopaedia Britannica., 2024).The tragedy not only marked a significant moment in maritime history but also revealed stark differences in survival rates among passengers based on their socio-economic status, age, gender, and class (Lord, 2005)

In the age of data science and machine learning, the Titanic dataset has become a widely used benchmark for learning and applying classification algorithms (Titanic, 2024).It offers a rich mix of categorical and numerical data, and allows for exploratory data analysis, visualization, and predictive modeling. By leveraging data-driven techniques, we can uncover patterns and relationships in the dataset that may have influenced the survival of passengers.

This project uses a subset of the Titanic passenger data to explore how different machine learning algorithms perform in predicting survival. We focus on three commonly used classification techniques—Logistic Regression, K-Nearest Neighbors (KNN), and Decision Tree—to develop models that estimate the probability of a passenger surviving the disaster. Each method offers unique strengths: logistic regression provides a probabilistic framework; KNN offers simplicity and intuitive logic; and decision trees bring interpretability and structure (James et al., 2013).

Beyond just model accuracy, this project aims to provide insights into the predictive power of various features and examine how well these algorithms generalize on unseen data. The findings can also demonstrate the potential and limitations of different algorithms when applied to real-world classification problems.

## Aim and Objectives

- Aim:
To build and compare classification models that predict the survival of passengers aboard the Titanic using different machine learning techniques in R.

- Objectives:
  
a) To explore, visualize, and preprocess the Titanic dataset for analysis.

b) To implement and apply three classification algorithms: Logistic Regression, K-Nearest Neighbours (KNN), and Decision Tree using R.

c) To evaluate and compare the performance of the models using metrics such as accuracy, confusion matrix, and ROC curves.

d) To interpret model results and identify key factors influencing passenger survival.

e) To demonstrate the end-to-end data science workflow using R, from data cleaning to predictive modelling and result interpretation.

## Data

The dataset used in this project is the Titanic: Machine Learning from Disaster dataset, available publicly on Kaggle. It contains detailed information about the passengers aboard the RMS Titanic, which sank on April 15, 1912.

- Data Source
  
Dataset name: Titanic - Machine Learning from Disaster
  
Source: Kaggle 

Format: CSV

Files Used:
train.csv – Used to build and train models

test.csv – Used for prediction

<img width="452" height="480" alt="image" src="https://github.com/user-attachments/assets/f9e01a54-da0d-429e-8c81-b94dde26e5c6" />

## Methodology

This study uses supervised learning algorithms to classify passengers' survival based on features in the Titanic dataset. The three classification techniques applied are:

[Logistic Regression](#logistic-regression)

[K-Nearest Neighbours](#k-nearest-neighbours)

[Decision Tree](#decision-tree)
  
All analyses were performed using R and packages like caret, ggplot2, rpart, and class.

- Data Preprocessing
  
Before modelling, the dataset underwent preprocessing:

a) Missing values in Age were filled with the median.

b) Missing Embarked values were replaced with the mode ("S").

c) Non-numeric variables were encoded as factors.

d) Irrelevant columns like Name, Ticket, and Cabin were dropped.

### Logistic Regression
  
Logistic Regression is a probabilistic, linear classifier used for binary classification. It models the probability of survival (1) versus not surviving (0).

Output :

<img width="452" height="230" alt="image" src="https://github.com/user-attachments/assets/923d78c5-311e-4457-963a-a00d5c07c116" />

- Significant Predictors:
  
a) Sexmale: Highly significant (p < 0.001)

b) Pclass2 and Pclass3: Usually significant

- Observations :
  
a) Being male and in lower class reduces odds of survival.

b) Higher fare and younger age slightly improved chances of survival.

- Evaluation, ROC curve and AUC output :

<img width="452" height="223" alt="image" src="https://github.com/user-attachments/assets/573b1621-c6b9-4fa8-b6d0-0b274700f107" />

Accuracy : 79.1 %

Sensitivity : 85.32 %

Specificity : 69.12 %

<img width="425" height="455" alt="image" src="https://github.com/user-attachments/assets/9d7753f3-f90d-4163-8304-0df9c5779435" />

<img width="452" height="88" alt="image" src="https://github.com/user-attachments/assets/ce52d7dd-deb9-4b60-83f8-b7e0b4516797" />

Expected AUC - 0.8408 (Strong classifier)

### K-Nearest Neighbours

KNN is a non-parametric algorithm that assigns class based on the majority of its k nearest neighbours in the feature space.
Preprocessing for KNN:

a) KNN requires scaled numerical variables.

b) Categorical variables were converted into dummy variables.

Output :

<img width="452" height="273" alt="image" src="https://github.com/user-attachments/assets/92cb9b3a-e685-4465-a60f-338476ace3c3" />

Accuracy = 76.27 %

Precision = 78.63%

Recall = 84.4%

- Observations:

a) Slightly lower accuracy than logistic regression.

b) Performs reasonably well but may misclassify some female or older passengers.

c) Confusion Matrix indicated some false positives, especially for predicting survival among males in 3rd class.

###  Decision Tree

Decision Trees split data into branches based on feature thresholds, forming a tree-like structure. It's intuitive and easy to visualize.

Output :

<img width="438" height="331" alt="image" src="https://github.com/user-attachments/assets/9de1a210-e697-48bc-a966-5f5b51ce895e" />

Tree Visualization clearly showed the most important decision rules , first split on Sex, then Pclass, followed by Fare and Age.

Female → more likely to survive

Male + 3rd class → less likely

- Confusion Matrix

Output :

  <img width="452" height="279" alt="image" src="https://github.com/user-attachments/assets/fb053fd3-ade0-420f-821f-f4b556cb170a" />

  Accuracy = 77.97%

## Visualization

1) Calculate the survival count

   <img width="452" height="427" alt="image" src="https://github.com/user-attachments/assets/193b6b57-3711-4218-8b29-1afe0bc8740a" />

- Survival Count Plot showed more passengers perished than survived.

2) Calculate the proportion of survival by gender .
  
  <img width="423" height="352" alt="image" src="https://github.com/user-attachments/assets/32867975-e4d4-45c3-9c9a-b737807efa8f" />

- Survival by Gender indicated females had a significantly higher survival rate, reflecting the “women and children first” evacuation policy.

3) Calculate the survival rate by passenger class.

   <img width="381" height="413" alt="image" src="https://github.com/user-attachments/assets/945a8e25-46ec-4294-8029-b0c6cfce5910" />

- Survival by Class confirmed higher survival rates among first-class passengers.

4) Calculate Age distribution by survival.

   <img width="337" height="315" alt="image" src="https://github.com/user-attachments/assets/cce94a5f-ce4e-4aa8-b0e0-a41502769bf3" />

- Age Distribution revealed that children had better survival chances, though many passengers in the 20–40 age group also survived.

## Results and discussion

  Logistic Regression, K-Nearest Neighbors (KNN), and Decision Tree — on the Titanic dataset. The goal was to predict passenger survival and evaluate each model’s performance based on classification accuracy, interpretability, and insights from the data.
  
- Logistic Regression Results
  
  Key Findings:
  
  - Sex (male): Strong negative predictor (males less likely to survive).
  - Pclass: Passengers in 3rd class were significantly less likely to survive.
  - Fare: Higher fare slightly increased survival probability.

  Performance Metrics:

  - Accuracy: 79.1%
  - AUC (ROC Curve):  0.8408 – indicating strong discrimination ability.
  - Confusion Matrix: High true positive rate for female passengers and those in higher classes.

   Interpretation:
  - The model supports the "women and children first" evacuation policy.
  - Logistic Regression was easy to interpret, making it ideal for explanatory purposes.
    
- K-Nearest Neighbors (KNN) Results
  
  Model Parameters:
  -Chosen value of k = 5 gave the best balance between bias and variance.
  
  Performance Metrics:
  - Accuracy: 76.27 %
  - Confusion matrix showed good performance for female passengers, but more errors in predicting survival of males.
    
  Observations:
  - Sensitive to data scaling and class imbalance.
  - Non-parametric approach worked reasonably well but lacked the interpretability of logistic regression.

- Decision Tree Results
  
  Visualization:
  - The tree split first on Sex, then Pclass, and Fare, confirming the same insights seen in logistic regression.
  - Clear path: Female + 1st class → high survival, Male + 3rd class → low survival.
    
  Performance Metrics:
  - Accuracy: 77.97%
  - Interpretability: High – easy to explain decisions visually using a tree diagram.
    
  Observations:
  - The tree captured non-linear interactions between features.
  - May overfit without pruning or cross-validation, though accuracy was comparable to logistic regression.

## Conclusion and Summary

This project used R to build and compare three classification models—Logistic Regression, KNN, and Decision Tree—to predict Titanic passenger survival. After cleaning and exploring the data, all models were evaluated on accuracy and interpretability.

- Logistic Regression performed the best (79.1% accuracy, AUC = 0.84) and clearly showed that gender, class, and fare were key predictors.
- KNN gave decent results (76.27%  accuracy) but was less interpretable.
- Decision Tree was highly visual and intuitive (77.97%  accuracy).
  
In conclusion, all models were effective, but Logistic Regression provided the best balance of performance and insights.


