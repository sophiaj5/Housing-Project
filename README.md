# Project 2 - Ames Housing Data and Kaggle Challenge

## Problem Statement

Given the ongoing inflationary trends affecting our current economy, it becomes increasingly important to seek out discounted prices, particularly when it comes to housing. The sale price of a house is influenced by a variety of factors that can either drive it up or down. Therefore, the primary goal of this project is to assess and compare the R2 scores of various models designed to predict house sale prices using different sets of variables.

## Data Dictionary

The data dictionary for this project can be found at:

https://www.kaggle.com/competitions/dsi-910-ames-housing-challenge/data


## Executive Summary

### Datasets and Models

For each model, both the train.csv and test.csv datasets were used to perform analysis on.

#### Datasets
1. train.csv (data used to train the model)
2. test.csv (data used to test the model (this data has SalePrice removed as this is our target to find))

#### Models
1. Model 1 - used a simple LinearRegression model
2. Model 2 - used a scaled LinearRegression model with PolynomialFeatures
3. Model 3 - used a scaled LinearRegression model with LassoCV

### Data Cleaning

Two different cleaning methods were used for the datasets to get an idea of different techniques that could be used. For Model 1, simply the missing values were removed and replaced with zeroes, as well as the data types were checked to make sure they all made sense. For Model 2 and Model 3, a custom function was written which replaced the missing values with either the mode of a column if it was an object, or the mean of the column if it was a numeric column. Again, the data types were checked for clarity, as well as a double check of missing values to ensure that the custom function worked for the two models.

### Exploratory Data Analysis

In order to test which model produced the best r2 score, many steps were taken. A train test split was used on the X (features) and y (target variable) and the variables were then fit on a LinearRegression model. After that, each model used its respective preprocessing steps (eg. PolynomialFeatures for Model 2) which then produced the r2 scores, along with other metrics, such as mean squared error. The r2 scores for each model were then compared to each other in comparison to the problem statement.


### Conlusions and Recommendations

In conclusion, the model that seemed to provide me the best r2 score was Model 2, which used a scaled LinearRegression model with PolynomialFeatures. This model produced a train model score of 0.91 and a test score of 0.90, which were the highest out of the three models. For further analysis for this project, different features for X could be looked at, as the same ones were used for this project. Additionally, more models could be added to see if a higher r2 score could be produced for the data. Finally, different techniques to clean the model could be used, such as dropping unnecessary columns or creating appropriate dummy variables. All of these could be great additions to add more depth to this project.