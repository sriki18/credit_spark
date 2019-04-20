# Predicting credit card defaulters

## Background

The dataset was downloaded from here: https://developer.ibm.com/blogs/snap-ml-use-cases-blog/ , credit default prediction. Quoting the text:

> The task in this use case is to predict whether a person who has credit will default (not be able to repay his credit). The data scientist is provided with a data set of 10 million transactions, each of which is characterized by 18 features (including account age, account type, credit history, owns car, transaction amount, and transaction category). Also provided are the labels of these transactions, default or not. The task is to build a model to predict whether transactions will default in an unseen data set, that is, a data set that has not been used to train the model and does not have labels.

The associated .csv data file is also available in this repository.

## Goal

- Binary classifcation : Predict whether a person who has credit will default or not be able to repay their credit.
- Interpretation : Use a regression framework to identify influential variables and quantify influence.

## Main challenges

- Size of dataset : 1 *million* rows * 19 columns. 
    - Favoring speed over ease of use, chose to use `Apache Spark` instead of `Pandas` and `sklearn`

## Software/Packages/Programs

### Major
Name | Version 
--- | ---
Python | 2.7
Apache Spark (`pyspark`) | 2.1.3

### Minor
Name | Version 
--- | ---
matplotlib | 1.5.0
seaborn | 0.7.1
NumPy | 1.13.1
Pandas | 0.17.1

## Service

- IBM Watson Studio Notebooks with Spark Service

## Status

- Logistic regression with untransformed features gives 97.7 % accuracy.
    - Pending : Test significance of coefficients.