# Car-Price-Prediction using Linear Regression

# Objective:
To predict the price of a car based on its features using regression algorithms and gain insights into what factors affect car pricing.

# Data Understanding:
Dataset has 205 rows and 27 columns.
Target column: price
Car-related features: CarName, fueltype, enginetype, cylindernumber, etc.

# Data Cleaning & Preparation:
Extracted company name from CarName column.
Fixed invalid car company names like:
maxda → mazda, porcshce → porsche, vokswagen → volkswagen, etc.
Converted all names to lowercase.
Checked and removed duplicates.
Converted numerical columns as needed.
Categorical features encoded using pd.get_dummies.

# Data Visualization:
Categorical Data Insights:
Most favoured car company: Displayed using countplot.
Fuel type comparison (gas vs diesel): Gas more common.
Car body preference, Engine types, Drive wheels, etc.
Boxplot of price → Identified outliers and skewness.

Numerical Data Insights:
Used pairplot to view relationships.
Found positive correlation with: enginesize, horsepower, curbweight.
Found negative correlation with: carwidth, peakrpm.

#Model Building (Linear Regression):
Train-Test Split: 80-20
Model Used: Linear Regression
Evaluation:
R² Score: ~0.82 (depending on train-test split)
Good fit, but some variance remains.

# Conclusion:
enginesize, curbweight, and horsepower are major factors affecting price.
fueltype, carbody, and drivewheel have significant categorical influence.
Regularization helps to improve generalization.
Final model can predict with reasonable accuracy (82.65%).
