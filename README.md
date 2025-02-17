# Used-Car-Price-Prediction---R-Data-Analytics
This repository contains an end-to-end Multiple Linear Regression model for predicting the price of used cars based on various features such as year, mileage, engine power, fuel type, and ownership history. The model is built using R and includes data cleaning, feature engineering, model training, and diagnostic checks.

📌 **Project Overview:**

🔹 Step 1: Data Loading & Cleaning
* Read the dataset (train-data.csv)
* Removed unnecessary column New_Price
* Converted Mileage, Engine, and Power to numeric values
* Handled missing values using the median

🔹 Step 2: Convert Categorical Variables
* Converted Location, Fuel Type, Transmission, and Owner Type to categorical factors

🔹 Step 3: Descriptive Statistics
* Summary statistics for key variables such as year, mileage, power, engine capacity, seats, and price
* Identified outliers in Kilometers Driven and Seats columns

🔹 Step 4: Build Multiple Regression Model
* Fitted a linear regression model to predict car prices:

model <- lm(Price ~ Year + Kilometers_Driven + Mileage + Engine + Power + Seats + Location + Fuel_Type + Transmission + Owner_Type, data = train_data)
* Extracted model coefficients to create an equation for price prediction

🔹 Step 5: Model Evaluation & Diagnostics
* Checked for Normality of Residuals: Used residual plots
* Checked for Multicollinearity: Used Variance Inflation Factor (VIF)
* Checked for Homoscedasticity: Plotted residuals against fitted values
* Checked for Independence of Residuals: Used Durbin-Watson Test

🏆 **Key Findings**
* Year of manufacture has a strong positive correlation with price.
* Mileage has a negative impact on price—cars with better mileage tend to have lower prices.
* Power and Engine Capacity significantly influence car pricing.
* Multicollinearity was detected in some variables, requiring further feature selection.
* The model needs further improvements by considering non-linear transformations or advanced ML models.
