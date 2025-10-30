# house-pricing
This project builds a Linear Regression model to predict housing prices (MEDV) in Boston using the classic Boston Housing dataset. The model aims to explain the variance in house prices based on various socio-economic and property-related features.

Features:
CRIM: Per capita crime rate by town
ZN: Proportion of residential land zoned for large lots
INDUS: Proportion of non-retail business acres
CHAS: Charles River dummy variable (1 if tract bounds river; 0 otherwise)
NOX: Nitric oxides concentration
RM: Average number of rooms per dwelling
AGE: Proportion of owner-occupied units built before 1940
DIS: Weighted distances to employment centers
RAD: Index of accessibility to radial highways
TAX: Full-value property tax rate
PTRATIO: Pupil-teacher ratio
B: Proportion of Black population
LSTAT: % lower status population

Target: MEDV - Median value of owner-occupied homes (in $1000s)

data preprocessing->
Missing Values: Filled using median.
Feature Transformations:
LSTAT → log(LSTAT + 1)
CRIM → sqrt(CRIM)

model training->
Train/Test Split: 80% train, 20% test.
Algorithm: Linear Regression (sklearn.linear_model.LinearRegression)
Training: On transformed features.

Metrics: R² score

Results:
Test R²: ~0.65–0.72
5-fold CV mean R²: ~0.64
Visualizations: Predicted vs Actual values, Feature importance, Residual Plot, Box Plot

Linear Regression captures ~65–72% of variance in Boston housing prices. Feature transformations improve linearity and performance. Cross-validation ensures reliable evaluation. This model serves as a baseline, with further improvement possible using polynomial features, regularization, or tree-based models.
