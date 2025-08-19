<img width="468" height="584" alt="image" src="https://github.com/user-attachments/assets/e2e4c919-f9e2-4b49-9bb1-34bfc1d9b7dd" /># -Survival-Prediction-on-the-Titanic-A-Comparative-Analysis-Using-Machine-Learning-Models-in-R-

[Introduction](#Introduction)

[Rationale](#rationale)

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

## Rationale

The field of data science has revolutionized how we interpret, understand, and derive insights from complex datasets. One of the most popular datasets in the data science community is the Titanic dataset, which offers a historical yet structured setting to apply and compare various machine learning algorithms. Despite its simplicity, the dataset reflects real-world characteristics—missing values, categorical variables, and non-linear relationships—that make it ideal for learning and testing classification models.
This project aims to not only predict survival outcomes using machine learning models but also to critically examine the effectiveness of different algorithms in doing so. The rationale behind choosing this dataset lies in its educational value, interpretability, and the rich context it provides. It bridges the gap between theoretical concepts and practical implementation by offering a meaningful and historic scenario in which modern-day analytics can be applied.
Moreover, the Titanic dataset provides a balanced challenge for both beginners and intermediate practitioners. It includes variables such as age, gender, ticket class, and fare—which can be intuitively understood by humans—allowing for the visualization and justification of model decisions. This interpretability is essential in evaluating not just how models perform but why they make certain predictions.
Another key reason for choosing this problem is that it allows for experimentation with a range of techniques, from basic statistical models like Logistic Regression to more complex algorithms like K-Nearest Neighbours (KNN) and Decision Trees. Each method brings unique strengths to the table—logistic regression provides explainability, KNN emphasizes proximity-based learning, and decision trees excel at rule-based segmentation. This project allows for a comparison of these approaches in terms of accuracy, usability, and interpretability, which is valuable for anyone aiming to work with predictive analytics in real-world scenarios.
Ultimately, this exercise is not just about building predictive models, but about enhancing understanding of the data, improving problem-solving skills, and gaining a deeper appreciation of the role machine learning plays in data-driven decision-making.

## Aim and Objectives

- Aim:
To build and compare classification models that predict the survival of passengers aboard the Titanic using different machine learning techniques in R.

- Objectives:
•	To explore, visualize, and preprocess the Titanic dataset for analysis.
•	To implement and apply three classification algorithms: Logistic Regression, K-Nearest Neighbours (KNN), and Decision Tree using R.
•	To evaluate and compare the performance of the models using metrics such as accuracy, confusion matrix, and ROC curves.
•	To interpret model results and identify key factors influencing passenger survival.
•	To demonstrate the end-to-end data science workflow using R, from data cleaning to predictive modelling and result interpretation.


