# Fraud Detection using Machine Learning in Python

## Overview

This documentation details the comprehensive steps and methodologies used to build a predictive algorithm for fraud detection using a training dataset. The objective is to create an accurate model to identify fraudulent transactions. The process is guided by Local Interpretable Model-agnostic Explanations (LIME) principles to ensure clarity and accessibility.

## Table of Contents

1. [Environment Set-up](#1-environment-set-up)
    - [Importing Libraries](#importing-libraries)
    - [Loading the Data](#loading-the-data)

2. [Initial Diagnostics](#2-initial-diagnostics)
    - [Data Overview](#data-overview)
    - [Descriptive Statistics](#descriptive-statistics)
    - [Target Variable Analysis](#target-variable-analysis)
    - [Predictor Variable Analysis](#predictor-variable-analysis)
    - [Correlation Matrix](#correlation-matrix)

3. [Data Processing](#3-data-processing)
    - [Handling Missing Values](#handling-missing-values)
    - [Managing Outliers](#managing-outliers)
    - [Removing Duplicate Observations](#removing-duplicate-observations)

4. [Exploratory Data Analysis](#4-exploratory-data-analysis)
    - [Analyzing Transaction Amounts](#analyzing-transaction-amounts)
    - [Time-Based Analysis of Fraud](#time-based-analysis-of-fraud)

5. [Class Imbalance Solutions](#5-class-imbalance-solutions)
    - [SMOTE (Synthetic Minority Oversampling Technique)](#smote-synthetic-minority-oversampling-technique)
    - [Near-Miss Algorithm](#near-miss-algorithm)
    - [Combined Sampling](#combined-sampling)

6. [Dimensionality Reduction](#6-dimensionality-reduction)
    - [Principal Component Analysis (PCA)](#principal-component-analysis-pca)
    - [Singular Value Decomposition (SVD)](#singular-value-decomposition-svd)
    - [Linear Discriminant Analysis (LDA)](#linear-discriminant-analysis-lda)

7. [Machine Learning Set-up](#7-machine-learning-set-up)
    - [Train-Test Split](#train-test-split)
    - [Cross-Validation](#cross-validation)

8. [Machine Learning Models](#8-machine-learning-models)
    - [Simple Models](#simple-models)
    - [Ensemble Methods](#ensemble-methods)

9. [Final Recommendation](#9-final-recommendation)

---

## 1. Environment Set-up

### Importing Libraries

- Libraries for data manipulation, visualization, statistical methods, sampling methods, model selection, dimensionality reduction, simple ML models, and ensemble learning are imported.
- Set a seed for reproducibility.

### Loading the Data

- Load the dataset using pandas to read the CSV file containing the transaction data.

---

## 2. Initial Diagnostics

### Data Overview

- Get a preliminary understanding of the dataset using functions like `df.info()` to check the structure and types of the data.

### Descriptive Statistics

- Use `df.describe()` to generate summary statistics of the dataset.

### Target Variable Analysis

- Analyze the distribution of the target variable to understand the class imbalance.

### Predictor Variable Analysis

- Examine the basic statistics and distribution of key predictors like the transaction amount.
- Use histograms and log-scale transformations to visualize data distributions.

### Correlation Matrix

- Create a correlation matrix to identify relationships between variables.
- Visualize correlations using a heatmap.

---

## 3. Data Processing

### Handling Missing Values

- Identify columns with missing values.
- Impute missing values using median or mode, depending on the data type.

### Managing Outliers

- Detect outliers using statistical methods like the z-score.
- Visualize outliers using boxplots and decide on handling strategies.

### Removing Duplicate Observations

- Identify and remove duplicate observations to ensure data quality.

---

## 4. Exploratory Data Analysis

### Analyzing Transaction Amounts

- Split the dataset into fraudulent and non-fraudulent transactions.
- Use histograms to compare the distribution of transaction amounts for both classes.
- Apply log transformation for better visualization.

### Time-Based Analysis of Fraud

- Plot transaction amounts over time to identify any time-based patterns in fraudulent activities.

---

## 5. Class Imbalance Solutions

### SMOTE (Synthetic Minority Oversampling Technique)

- SMOTE is used to oversample the minority class by creating synthetic examples.

### Near-Miss Algorithm

- This undersampling technique selects examples from the majority class that are close to the minority class examples.

### Combined Sampling

- Apply both oversampling and undersampling techniques to balance the dataset.

---

## 6. Dimensionality Reduction

### Principal Component Analysis (PCA)

- Reduce the number of features while retaining most of the variance in the data.

### Singular Value Decomposition (SVD)

- Decompose the data matrix into singular vectors and values for dimensionality reduction.

### Linear Discriminant Analysis (LDA)

- Use LDA to project data in a way that maximizes class separability.

---

## 7. Machine Learning Set-up

### Train-Test Split

- Split the data into training and testing sets to evaluate model performance.

### Cross-Validation

- Implement cross-validation techniques to ensure robust model evaluation.

---

## 8. Machine Learning Models

### Simple Models

- Logistic Regression
- k-Nearest Neighbors (k-NN)
- Decision Tree
- Stochastic Gradient Descent (SGD)

### Ensemble Methods

- Random Forest
- Stochastic Gradient Boosting
- Stacking

---
