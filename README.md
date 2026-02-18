# CO₂ Emissions Analysis — Vehicle Dataset
This project investigates the factors that drive vehicle CO₂ emissions, using a publicly available dataset containing vehicle specifications, fuel consumption metrics, engine details, and rated emissions.
The analysis explores three core objectives:

Determine the importance of different variables on CO₂ emissions

Evaluate predictive performance of multiple modeling approaches

Assess whether considering City/Highway fuel consumption separately differs from using a weighted combined metric

## 1. Dataset Overview
The dataset includes vehicle-level attributes such as:

Engine size

Cylinders

Transmission and fuel type

Fuel consumption (City, Highway, Combined)

CO₂ emissions (target variable)

Initial preprocessing included:

Removing non-predictive ID-like columns (Make, Model)

Encoding categorical variables (Transmission, Fuel Type)

Scaling numeric variables for linear models

Cleaning column names for consistency

## 2. Exploratory Data Analysis
Correlation Insights

A correlation heatmap was generated to examine linear relationships.
Key observations:

Fuel Consumption City and Fuel Consumption Highway showed the strongest correlation with CO₂ emissions.

Engine Size and Cylinders also correlated positively.

Categorical variables (once one-hot encoded) showed weaker direct correlations, as expected.

This guided model design and feature engineering.

## 3. Modeling Approaches
To rigorously evaluate variable importance, three independent strategies were used:

A. Linear Regression (OLS Model)

A baseline multivariate linear regression was trained on standardized features.

Provided interpretable coefficients

Confirmed Fuel Consumption City as the strongest linear driver

Showed moderate R² due to linearity limitations

B. Random Forest Regressor (Tree-Based Model)

A 300-tree ensemble model was fitted to capture nonlinear effects.

Produced a ranked Feature Importance Table

Top features:

Fuel Consumption City

Fuel Consumption Highway

Engine Size

Cylinders

Fuel-type-related dummy variables contributed, but less significantly

This model produced the highest predictive power among all tested models.

## Key Conclusions
Fuel consumption metrics are the strongest predictors of CO₂ emissions.

City consumption impacts emissions more heavily than highway.

Engine size and cylinder count also contribute meaningfully.

Random Forest provided a robust explanation framework.

Separating City and Highway fuel metrics gives deeper insight than using the combined weighted metric.\

# Tools & Libraries Used :
Python (Pandas, NumPy)

Scikit-Learn

Seaborn, Matplotlib
