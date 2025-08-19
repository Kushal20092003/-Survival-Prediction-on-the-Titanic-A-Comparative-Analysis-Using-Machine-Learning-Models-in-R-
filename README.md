# -Survival-Prediction-on-the-Titanic-A-Comparative-Analysis-Using-Machine-Learning-Models-in-R-

[Introduction](#Introduction)

[Aim and Objectives](#aim-and-objectives)

[Data](#data)

[Methodology](#methodology)

[Results and discussion](#results-and-discussion)

[Counclusion and Summary](#counclusion-and-summary)

[References](#references)


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
- K-Nearest Neighbours (KNN)
- Decision Tree
  
All analyses were performed using R and packages like caret, ggplot2, rpart, and class.

- Data Preprocessing
  
Before modelling, the dataset underwent preprocessing:

a) Missing values in Age were filled with the median.

b) Missing Embarked values were replaced with the mode ("S").

c) Non-numeric variables were encoded as factors.

d) Irrelevant columns like Name, Ticket, and Cabin were dropped.

### Logistic Regression
  
Logistic Regression is a probabilistic, linear classifier used for binary classification. It models the probability of survival (1) versus not surviving (0).

<img width="452" height="230" alt="image" src="https://github.com/user-attachments/assets/923d78c5-311e-4457-963a-a00d5c07c116" />

