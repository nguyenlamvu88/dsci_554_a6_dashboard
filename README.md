# Acute Inflammations and Violent Crimes Analysis

## Overview

This repository presents a comprehensive analysis and predictive modeling project addressing two distinct datasets:

1. **Acute Inflammations Dataset:** Focused on building interpretable Decision Tree models to predict inflammation of the bladder.
2. **Communities and Crime Dataset:** Involves data cleaning, exploratory data analysis (EDA), feature engineering, and implementing various regression models, including Linear Regression, Ridge Regression, LASSO, Principal Component Regression (PCR), and XGBoost to predict violent crimes per population.

The project is structured to meet specific assignment requirements, facilitating a clear understanding of data preprocessing, model building, evaluation, and interpretation across both classification and regression tasks.

## Table of Contents

- [Overview](#overview)
- [Datasets](#datasets)
- [Installation](#installation)
- [Usage](#usage)
  - [1. Decision Trees as Interpretable Models](#1-decision-trees-as-interpretable-models)
    - [1.a. Download Acute Inflammations Data](#1a-download-acute-inflammations-data)
    - [1.b. Build and Plot Decision Tree](#1b-build-and-plot-decision-tree)
    - [1.c. Convert Decision Rules to IF-THEN Statements](#1c-convert-decision-rules-to-if-then-statements)
    - [1.d. Cost-Complexity Pruning](#1d-cost-complexity-pruning)
  - [2. The LASSO and Boosting for Regression](#2-the-lasso-and-boosting-for-regression)
    - [2.a. Download and Split Communities and Crime Data](#2a-download-and-split-communities-and-crime-data)
    - [2.b. Handle Missing Values and Ignore Nonpredictive Features](#2b-handle-missing-values-and-ignore-nonpredictive-features)
    - [2.c. Plot Correlation Matrix](#2c-plot-correlation-matrix)
    - [2.d. Calculate Coefficient of Variation (CV)](#2d-calculate-coefficient-of-variation-cv)
    - [2.e. Select Top Features and Generate Plots](#2e-select-top-features-and-generate-plots)
    - [2.f. Fit Linear Regression Model](#2f-fit-linear-regression-model)
    - [2.g. Fit Ridge Regression Model](#2g-fit-ridge-regression-model)
    - [2.h. Fit LASSO Regression Model](#2h-fit-lasso-regression-model)
    - [2.i. Fit Principal Component Regression (PCR) Model](#2i-fit-principal-component-regression-pcr-model)
    - [2.j. Fit XGBoost Regressor](#2j-fit-xgboost-regressor)
- [Results](#results)
- [License](#license)

## Datasets

1. **Acute Inflammations Dataset**  
   [UCI Machine Learning Repository: Acute Inflammations](https://archive.ics.uci.edu/ml/datasets/Acute+Inflammations)

2. **Communities and Crime Dataset**  
   [UCI Machine Learning Repository: Communities and Crime](https://archive.ics.uci.edu/ml/datasets/Communities+and+Crime)

## Installation

Ensure you have Python 3.7 or higher installed. Follow the steps below to set up the environment:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/acute-inflammations-violent-crimes-analysis.git
   cd acute-inflammations-violent-crimes-analysis```

2. **Install the required packages:**

   ```bash
   pip install -r requirements.txt
   ```

Alternatively, install the packages directly:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost chardet
   ```

## Usage

The analysis is conducted using a single Jupyter Notebook that sequentially addresses all assignment requirements. Follow the steps below to execute the analysis:

### 1. Decision Trees as Interpretable Models

#### 1.a. Download Acute Inflammations Data
- **Objective:** Acquire the Acute Inflammations dataset from the UCI repository.
- **Action:** Download and load the dataset, ensuring correct encoding and data integrity.

#### 1.b. Build and Plot Decision Tree
- **Objective:** Construct a Decision Tree classifier using the entire Acute Inflammations dataset.
- **Action:** Train the Decision Tree model and visualize its structure to understand feature importance and decision pathways.

#### 1.c. Convert Decision Rules to IF-THEN Statements
- **Objective:** Translate the trained Decision Tree into a set of interpretable IF-THEN rules.
- **Action:** Extract decision rules to facilitate easy interpretation and application in practical scenarios.

#### 1.d. Cost-Complexity Pruning
- **Objective:** Simplify the Decision Tree to enhance interpretability and prevent overfitting.
- **Action:** Apply cost-complexity pruning to obtain a minimal tree structure with high interpretability, refining the decision rules accordingly.

### 2. The LASSO and Boosting for Regression

#### 2.a. Download and Split Communities and Crime Data
- **Objective:** Acquire the Communities and Crime dataset and prepare it for analysis.
- **Action:** Download the dataset, load it into the environment, and split it into training (first 1495 rows) and testing sets (remaining rows).

#### 2.b. Handle Missing Values and Ignore Nonpredictive Features
- **Objective:** Clean the dataset by addressing missing values and removing nonpredictive features.
- **Action:** Impute missing data using an appropriate imputation technique (e.g., median imputation) and exclude features identified as nonpredictive based on the data description.

#### 2.c. Plot Correlation Matrix
- **Objective:** Explore relationships between features in the Communities and Crime dataset.
- **Action:** Compute and visualize the correlation matrix to identify multicollinearity and potential predictor variables.

#### 2.d. Calculate Coefficient of Variation (CV)
- **Objective:** Assess the variability of each feature relative to its mean.
- **Action:** Calculate the Coefficient of Variation (CV) for each feature to identify those with the highest variability.

#### 2.e. Select Top Features and Generate Plots
- **Objective:** Focus analysis on the most variable features to uncover significant patterns.
- **Action:** Select the top √128 (approximately 11) features with the highest CV and generate scatter plots and box plots to visualize their distribution and relationship with the target variable. Discuss any observable significance from these visualizations.

#### 2.f. Fit Linear Regression Model
- **Objective:** Establish a baseline predictive model for violent crimes per population.
- **Action:** Train a Linear Regression model using least squares on the training set and evaluate its performance on the test set by reporting the test error metrics.

#### 2.g. Fit Ridge Regression Model
- **Objective:** Enhance the baseline model by addressing multicollinearity through regularization.
- **Action:** Train a Ridge Regression model with the regularization parameter (λ) chosen via cross-validation and report the test error metrics.

#### 2.h. Fit LASSO Regression Model
- **Objective:** Perform feature selection and improve model interpretability.
- **Action:** Train a LASSO Regression model with λ selected by cross-validation, report the test error, and list the variables selected by the model. Repeat the process with standardized features and compare the test errors to assess the impact of feature scaling.

#### 2.i. Fit Principal Component Regression (PCR) Model
- **Objective:** Reduce dimensionality while retaining essential variance in the data.
- **Action:** Apply Principal Component Analysis (PCA) to determine the optimal number of principal components (M) through cross-validation, train a Linear Regression model using these components, and report the test error metrics.

#### 2.j. Fit XGBoost Regressor
- **Objective:** Leverage advanced boosting techniques to improve predictive performance.
- **Action:** Train an XGBoost Regressor with hyperparameters (including α for regularization) optimized via cross-validation and report the test error metrics.

## Results

The analysis encompasses both classification and regression tasks, providing insights and predictive capabilities for each dataset:

### 1. Acute Inflammations Dataset

- **Decision Trees:**
  - **Initial Model:** Demonstrated the ability to capture complex patterns but exhibited overfitting.
  - **Pruned Model:** Achieved a balance between complexity and interpretability, enhancing the model's generalization to unseen data.
  - **Decision Rules:** The extracted IF-THEN rules offer clear insights into the factors influencing bladder inflammation, facilitating informed decision-making.

### 2. Communities and Crime Dataset

#### Data Cleaning and Preparation:
- Successfully handled missing values through median imputation and excluded non-predictive features, ensuring data integrity and relevance.

#### Exploratory Data Analysis:
- **Correlation Matrix:** Identified key relationships between socio-economic factors and violent crime rates, highlighting potential predictors.
- **Coefficient of Variation (CV):** Selected features with the highest variability, indicating their potential significance in predicting violent crimes.
- **Visualizations:** Scatter plots and box plots provided visual evidence of feature distributions and their relationships with the target variable, guiding feature selection and model focus.

#### Regression Models:
- **Linear Regression:** Served as a baseline model, establishing initial predictive performance metrics.
- **Ridge Regression:** Improved model performance by mitigating multicollinearity through regularization.
- **LASSO Regression:** Enabled feature selection, identifying the most influential predictors and simplifying the model without compromising performance.
- **Principal Component Regression (PCR):** Achieved dimensionality reduction while maintaining model performance, optimizing the number of principal components for balance between complexity and accuracy.
- **XGBoost Regressor:** Delivered superior predictive capabilities through advanced boosting techniques and meticulous hyperparameter tuning, outperforming traditional regression models.

#### Model Evaluation:
- Metrics like Mean Squared Error (MSE) and Root Mean Squared Error (RMSE) were consistently used to evaluate and compare model performances, providing quantitative measures of predictive accuracy.


