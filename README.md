# Ames House Price Prediction

## Project Overview

This project analyses the Ames housing dataset to understand the factors that influence house prices. In this project, I will apply data analysis and machine learning techniques to explore and build predictive models based on the housing features to prect the sale price of the houses.

## Problem statement

House prices are influnced by multiple factors such as; size, location, year of construction, characteristics of the neighborhood and many more.

Due to the Real estate market's complexity, this project aims to analyze housing features and develop a  predictive model that estimates house prices based on the Ames housing dataset.

## Project Objectives

(i) Explore and understand the Ames Housing dataset

(ii) Identify the factors affecting house prices

(iii) Perform exploratory data analysis (EDA)

(iv) Clean and prepare the data for modeling

(v) Build a machine learning model to predict house prices

(vi) Evaluate the performance of the model


## Dataset Description

The Ames Housing dataset contains detailed information about residential homes in Ames, Iowa, USA. The dataset includes 79 explanatory variables describing different aspects of houses and one target variable called **SalePrice**, which will be the final selling price of the property.

Example variables include:

OverallQual – Overall material and finish quality

 GrLivArea – Above ground living area (square feet)

 GarageCars – Garage size in car capacity

 TotalBsmtSF – Total basement area

 YearBuilt – Year the house was built

 Neighborhood – Location within Ames


 ## Data source 

The dataset i used in this project is **Ames Housing dataset** and its available on Kaggle

**Source**https://www.kaggle.com/datasets/rishitaverma02/house-prices-advanced-regression-techniques


## Tools and Technologies 

Python 

Pandas

Jupyter notebook

matplotlib

seaborn

numpy

## Data cleaning

I first checked for the missing values in the dataset and then I dropped the columns with more than 50% missing values and filled the missing values in the numerical columns with the median value and in the categorical columns with the mode value. Finally, I checked for duplicate rows and found that there are no duplicate rows in the dataset. 

Outliers were detected using the Interquartile Range (IQR) method and removed from the dataset so that i cn improve the performance of the model. 


## Exploratory Data Analysis (EDA)  

EDA will help me discover patterns, relationships and insights in the data.

# 1. Summary Statistics
Summary statistics provide a quick overview of the central tendency, dispersion and shape of the distribution of the house prices.


# 2. Distribution of house prices
i did distribution of house prices to understand are prices nomally distributed, are there extremely expensive houses or is the data skewed.

**interpretation**
The distribution is right skewed,most houses cost between $100,000-$200,000 and there are some expensive houses that cost more than $300,000.This means that most houses and affordable but few luxury houses that are expensive hence increase the maximum price.
Through a histogram i was able to visualize the distribution of the house price and the central tendancy of the data

# 3. Correlation analysis
i did correlation analysis to know which variables influences the house prices the most.

**Interpretation**
The most positively correlated variable with SalePrice is OverallQual (0.79), which indicates that house quality has a strong influence on the price. GrLivArea (0.71) also shows a strong positive correlation, suggesting that larger living areas tend to increase house prices. GarageCars (0.62) indicating more garage space increase house prices. 

# 4. Relationship Between OverallQual and SalePrice
correlation gave numbers but with scatterplot i was able to visualize the actual relationship.

**Interpretation**
Each dot represents a house, and the plot shows that as House Quality increases, SalePrice also tends to increase, confirming the strong positive correlation between these two variables.

# 5. Boxplot for Categorical features
Here i wanted to see which Neighborhood have expensive houses

**Interpretation**
The boxplot comparing SalePrice across neighborhoods reveals significant variation in housing prices based on location. Certain neighborhoods such as NridgHt and StoneBr exhibit higher median house prices, therefore these areas are more desirable . Conversely, neighborhoods like NPKVill and Blueste have lower median prices, indicating relatively more affordable housing.


## Feature Engineering

Here i improve the input data so that the machine learning model can make better predictions.
Models need numerical data to make prediction so i converted the categorical data into numerical data using one-hot encoding. This process creates new binary columns for each category in the original categorical feature, allowing the model to interpret and utilize this information effectively.

## Train-Test Split
Here i split the data so that i can test if the model generalizes to the new data that it hasnt seen before.
If i train and test on the same data the model will memorize the dataset and this will lead to overfitting and bad performance on the new data.
So i splitted the data into training data(this will teach the model) and testing data(this will evaluate performance )
80% training
20% testing


## Training a Machine Learning Model
i trained a model that can learn;  the relationship between the features and the target variable (SalePrice) so that it can make predictions on new data.(X_train → y_train)

I used Linear Regression which is a simple and widely used algorithm for regression problems. It assumes a linear relationship between the features and the target variable, making it a good starting point for this problem. 

 


