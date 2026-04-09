# 🏠 House Price Prediction — Multiple Linear Regression

## Overview
A machine learning project that builds and compares predictive models to estimate house prices based on property features. The dataset was loaded from **Azure Blob Storage** and analysed using **Python**, with models evaluated using RMSE and visualised through scatter plots and correlation heatmaps.

## Dataset
Sourced from Azure Blob Storage — `house_sales_prediction.csv`

Features used to predict house price:
- `Square_Feet` — total area of the house
- `Num_Bedrooms` — number of bedrooms
- `Num_Bathrooms` — number of bathrooms
- `Num_Floors` — number of floors
- `Garage_Size` — size of the garage
- `Location_Score` — desirability score of the location
- `Distance_to_Center` — distance to city centre (km)
- `Price` — target variable

## Steps Completed

**Step 1 — Loading & Understanding the Data**
- Connected to Azure Blob Storage and loaded the dataset into a Pandas DataFrame
- Inspected data types, null values, and initial structure

**Step 2 — Exploratory Data Analysis (EDA)**
- Computed summary statistics
- Visualised the relationship between square footage and price via scatter plot
- Plotted the price distribution using a histogram
- Computed and visualised a correlation heatmap — identified `Square_Feet` and `Num_Bedrooms` as the dominant price drivers

**Step 3 — Multiple Linear Regression (MLR)**
- Split data into features (X) and target (y)
- Split into 80% training and 20% testing sets
- Trained a Multiple Linear Regression model
- Visualised actual vs predicted prices
- Evaluated using RMSE — **~$63,952**

**Step 4 — Random Forest Regressor**
- Trained a Random Forest model (100 estimators) on the same data
- Visualised actual vs predicted prices
- Evaluated using RMSE — **~$71,733**
- Compared both models — MLR outperformed Random Forest on this dataset

**Step 5 — Conclusion & Insights**
- MLR performed better due to the largely linear nature of the relationships in the dataset
- Random Forest underperformed as the data lacks the complex non-linear patterns it is designed to capture
- Recommendations for further improvement discussed, including feature engineering and hyperparameter tuning

## Tools & Skills
`Python` · `Pandas` · `Scikit-learn` · `Seaborn` · `Matplotlib` · `Azure Blob Storage` · `Linear Regression` · `Random Forest` · `RMSE Evaluation` · `EDA`
