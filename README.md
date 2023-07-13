# Thyroid Disease Classification

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
    - [Handling Missing Values](#handling-missing-values)
    - [Feature Selection](#feature-selection)
    - [Handling Imbalanced Data with Oversampling](#handling-imbalanced-data-with-oversampling)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Results](#results)
- [Conclusion](#conclusion)
- [Accessing the Jupyter Notebook](#accessing-the-jupyter-notebook)

## Overview
This project focuses on building a robust classification model to predict the presence or absence of thyroid disease based on various patient attributes. The dataset used for this project contains information about patients' demographic, medical, and laboratory features.

## Dataset
The dataset used in this project consists of X entries and Y features. The target variable, binaryClass, indicates the presence or absence of thyroid disease. The dataset is initially imbalanced, with a majority class and a minority class.

## Data Preprocessing

### Handling Missing Values
The dataset contained missing values in certain columns. Missing values were imputed using the median value of the respective column. This approach was chosen because median is less sensitive to outliers compared to the mean, providing a more robust imputation strategy.

### Feature Selection
To select the most relevant features for the classification task, the chi-square test was performed. The chi-square test measures the dependence between categorical features and the target variable. The selected features were chosen based on their high association with the target variable, indicating their potential predictive power. The selected features are: 'on thyroxine', 'query hypothyroid', 'TSH', 'TT4', and 'FTI'.

### Handling Imbalanced Data with Oversampling
The dataset initially had an imbalanced class distribution, with a majority class and a minority class. To address this issue, the SMOTE-NC (Synthetic Minority Over-sampling Technique for Nominal and Continuous) algorithm was applied. SMOTE-NC oversamples the minority class by generating synthetic samples that resemble the existing minority class samples. This technique helps to balance the class distribution, preventing the model from being biased towards the majority class.

## Model Training and Evaluation
For the classification task, several machine learning models were trained and evaluated using the preprocessed dataset. The following models were used: Random Forest, SVM (Support Vector Machine) and KNN (K-Nearest Neighbors).

Each model was trained using the selected features and evaluated using various metrics including accuracy, precision, recall, F1 score, confusion matrix, and classification report. Grid search was applied to optimize the hyperparameters of the models, resulting in improved performance.

## Results
The performance of the models on the test set is as follows:
- Random Forest: Accuracy of 99.3%
- KNN: Accuracy of 96.6%
- SVM: Accuracy of 95.7%

Please refer to the individual model training code for detailed evaluation metrics and performance results.

## Conclusion
In this project, I successfully developed a classification model for predicting thyroid disease based on patient attributes. The preprocessing steps, including handling missing values, feature selection, and oversampling, helped to improve the quality of the dataset and address challenges related to imbalanced data. The trained models demonstrated high accuracy, indicating their effectiveness in predicting thyroid disease.

## Accessing the Jupyter Notebook
To access the Jupyter Notebook containing the code and analysis for this project, please follow the steps below:
1. Clone or download the repository from the GitHub link: [GitHub Repository](https://github.com/kanishkmunot/Thyroid_prediction.git)
2. Open Jupyter Notebook or JupyterLab on your local machine.
3. Navigate to the directory where you cloned or downloaded the repository.
4. Open the Jupyter Notebook file (.ipynb) to view and run the code.



Feel free to explore the notebook and interact with the code to gain further insights into the project.
