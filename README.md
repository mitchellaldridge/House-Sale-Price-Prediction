# House-Sale-Price-Prediction

## Overview
The projects goal is to predict house sale prices based on a variety of home related predictor variables.

## Data
The data is from the Kaggle Competition House Prices - Advanced Regression Techniques

## Methodology
### Step 1: Exploratory Data Analysis
- Using libraries such as pandas and matplotlib to sort the data and visualize different trends and correlations between the variables.
- Used a log transformation on the reponse variable to reduce a large right skew.
### Step 2: Data Cleaning
- Used scikit-learns Pipelines to build a imputer for missing data, using median and standard scaler on numerical variables and most frequent values and one hot encoding for categorical variabels.
### Step 3: Model Selection
- Used 5 fold cross validation on Linear models such as Linear, Ridge, Lasso and Elastic Net regression models, as well as on tree models such as RandomForest, XGBoost, Gradient Boosting, and LightGBM.
- Compared the models based on RMSE scores, and selected the best performing model, XGBoost, to do hyperparameter tuning on to further improve RMSE.
### Step 4: Hyperparameter Tuning
- Used RandomizedSearchCV from scikit-learn to find optimal hyperparameters for the XGBoost model.

## Results
- The reuslts showed that tree based models outperformed linear models for predicting future home sales.
- A final Cross Validation RMSE score of 0.12 was found for the best model on the logged response variable.
