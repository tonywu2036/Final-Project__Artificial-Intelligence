# Final-Project__Artificial-Intelligence# 🍷 Wine Quality Prediction – Machine Learning Final Project

This repository contains my final project for predicting red wine quality using machine learning models.  
The project includes feature engineering, model training, evaluation, and a summary of findings.


##  Abstract

This project analyzes the Red Wine Quality dataset from the UCI Machine Learning Repository and builds two machine learning models—Logistic Regression and Random Forest—to perform multi-class classification of wine quality. All 11 physicochemical attributes in the dataset are numerical and were used as input features. Logistic Regression achieved an accuracy of 0.59, while Random Forest performed significantly better with 0.68 accuracy. Both models struggled with minority classes due to class imbalance. The results align with findings in the literature, which indicate that ensemble tree-based models are well-suited for this dataset. Future improvements may include oversampling techniques and advanced ensemble methods such as XGBoost.


##  Dataset

**Source:** UCI Machine Learning Repository  
**Dataset:** Red Wine Quality  
**Samples:** 1,599  
**Target Variable:** `quality` (integer 3–8)  
**Features (all numerical):**

- fixed acidity  
- volatile acidity  
- citric acid  
- residual sugar  
- chlorides  
- free sulfur dioxide  
- total sulfur dioxide  
- density  
- pH  
- sulphates  
- alcohol  

The goal is to predict wine quality as a multi-class classification task.


##  Feature Engineering

- All 11 features were used for training.
- All features are **numerical**, so no categorical encoding was required.
- The label `quality` was separated from the input features.
- **StandardScaler** was applied only to Logistic Regression.
- Random Forest was trained without scaling since tree-based models are scale-invariant.
- No features were dropped because all chemical attributes contribute to wine quality.


##  Models Used

### 1. Logistic Regression
- Used as a baseline model.
- Requires feature scaling.
- Performs well for linear relationships.

### 2. Random Forest Classifier
- Ensemble method consisting of multiple decision trees.
- Captures non-linear patterns.
- Provides feature importance analysis.
- Does not require scaling.


##  Results

| Model                | Accuracy |
|----------------------|----------|
| Logistic Regression  | **0.59** |
| Random Forest        | **0.68** |

### Key Observations
- Random Forest outperformed Logistic Regression.
- Both models struggled with rare classes (quality 3, 4, 8).
- Class imbalance is a significant challenge for this dataset.
- Middle classes (5 and 6) dominate predictions.

##  Confusion Matrices (Summary)

### Logistic Regression
- Strong bias toward predicting classes 5 and 6.
- Nearly zero recall for minority classes.
- Accuracy: 0.59.

### Random Forest
- More balanced predictions across classes.
- Improved recall and precision.
- Accuracy: 0.68.


##  Video Presentation

 **Video Link:**: https://youtu.be/7WRxvsRxEGk  
The video provides a walkthrough of the dataset, notebook, models, and key findings.


## Jupyter Notebook

 **Notebook Link:** :https://colab.research.google.com/drive/1_JGZfyw8J2X6YRnppXTdCscuXaekPyrs#scrollTo=_IO0BHNYqWwI

You can open the notebook directly on GitHub or download it to run locally or in Google Colab.


