# Decision tree
# COVID Tested Patient Dataset Analysis Using Machine Learning
This project applies various machine learning techniques to classify COVID-19 test results based on a comprehensive dataset. The goal is to identify the most effective machine learning model for accurate and reliable predictions, contributing to a better understanding and management of COVID-19.

### Table of Contents
Overview

Dataset

Data Preprocessing

Exploratory Data Analysis (EDA)

Modeling

Evaluation

Technologies Used


Key Steps in the Workflow

### Overview
Early detection and accurate classification of COVID-19 test results are critical for controlling the spread of the virus and improving patient outcomes. This project uses machine learning algorithms to classify COVID-19 test results based on a range of symptoms and demographic data. The models evaluated include Decision Tree and Random Forest to determine the most effective classifier.

### Key Goals:
Build a robust and scalable pipeline for data preprocessing, training, and evaluation.

Leverage cross-validation to enhance model reliability.

Visualize data relationships and identify correlations between features.

### Dataset
The dataset used in this project was obtained from Kaggle:

COVID Tested Patient Dataset

Features:
Symptoms (e.g., Cough, Fever, Sore throat, Shortness of breath, Headache).

Demographic data (e.g., Sex, Known contact with COVID-19 case).

A categorical target variable: COVID-19 test result (positive, negative, other).

### Data Preprocessing
Loading and Cleaning Data:
Removed unnecessary columns (e.g., Age_60_above, Ind_ID, Test_date).

Addressed missing values by dropping rows with null values.

#### Feature Selection:
Retained relevant columns for analysis.

Applied label encoding to the target column (COVID-19 test result).

#### Train-Test Split:
Data split into 80% training and 20% testing subsets.

### Exploratory Data Analysis (EDA)
Visualized feature distributions and relationships to identify important predictors for COVID-19 diagnosis.

### Modeling
Models Implemented:
Decision Tree:
Parameters: criterion='gini'.

Achieved an accuracy of approximately 95.76%.

Random Forest:
Parameters: criterion='gini'.

Achieved an accuracy of approximately 95.76%.

Evaluation
Cross-validation was used to ensure robust model performance across multiple folds. Both the Decision Tree and Random Forest models demonstrated similar effectiveness for this dataset.

### Model Evaluation Metrics:
Accuracy: Percentage of correctly classified instances.

Confusion Matrix: Summary of prediction results.

Classification Report: Precision, recall, and F1-score for each class.

Model Evaluation
1. Decision Tree Classifier:
Achieved a test accuracy of 95.76%, indicating strong performance on the test dataset.

Precision, Recall, and F1-Score:

High performance for the majority class (negative) but struggled to identify minority classes (positive and other).

The precision for the -1 class (representing "other") was ill-defined due to a lack of predictions.

Confusion Matrix:

Showed strong accuracy for the negative class but highlighted misclassifications for the other classes.

2. Random Forest Classifier:
Delivered the same test accuracy as the Decision Tree (95.76%).

Classification Metrics:

Similar metrics to the Decision Tree, with a weighted average F1-score of 0.95.

The model did not improve the ability to classify the -1 class effectively.

#### Comparison Between Models
###### Strengths:

Both models demonstrated high accuracy for the dominant class (negative), suggesting they are well-suited for majority-class predictions.

Random Forest, with its ensemble approach, typically offers better generalization, but the performance was comparable to the Decision Tree here.

##### Weaknesses:

Both models struggled with class imbalance. The minority class (-1) had no correct predictions, leading to ill-defined precision.

Addressing Class Imbalance:

Employ oversampling (e.g., SMOTE) or undersampling techniques to balance the classes.

Technologies Used
Programming Language: Python

Libraries:

pandas, numpy for data manipulation

matplotlib, seaborn for visualization

scikit-learn for machine learning
