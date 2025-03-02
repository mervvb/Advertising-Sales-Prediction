 # Advertising Sales Prediction
# A. Dataset Citation:
# Kaggle. (2023). Advertising Sales Dataset. Retrieved from 
# https://www.kaggle.com/datasets/yasserh/advertising-sales-dataset
# This dataset contains advertising spending across different media (TV, radio, and newspaper) and the corresponding sales figures.  -->

 # B. Technologies
# This project uses the following Python libraries and tools:

# - Python 3.12
# - **pandas**: Used for data manipulation and analysis.
# - **numpy**: Used for numerical computations and handling arrays.
# - **matplotlib**: Used for data visualization, specifically for creating plots and graphs.
# - **scikit-learn**: A machine learning library used for model building, training, and evaluation.
# - **StandardScaler**: Used for feature scaling to standardize the dataset.
# - **LinearRegression**: Used to implement multiple linear regression models.
# - **train_test_split**: Used for splitting the dataset into training and testing sets.
# - **mean_squared_error**: Used for evaluating the performance of regression models.
# - **r2_score**: Used for calculating the R² (coefficient of determination) score for model evaluation.
# - **statsmodels**: A library used for statistical modeling.
# - **variance_inflation_factor**: Used to calculate the Variance Inflation Factor (VIF) to assess multicollinearity.
# - **add_constant**: Used to add a constant to the model for regression analysis.
 
# C. Results:

# 1. Simple Linear Regression Models

# a) For every $1 increase in TV advertising budget, sales increase by $3.9157 on average
# b) For every $1 increase in Radio advertising budget, sales increase by $3.0168 on average.
# c) For every $1 increase in Newspaper advertising budget, sales increase by only $1.2114 on average.
# d) A company should prioritize TV and Radio over Newspaper ads for better returns.
# e) If the budget is limited, spending more on TV ads will likely maximize sales growth.
# f) Newspaper Advertising might be less effective, so investing too much in it may not be cost-efficient.

# 2. Multiple Linear Regression Model
# a) The model explains a good portion of the sales variation with a high R² value (88.6%).
# b) The reason you're seeing a much higher R² when using multiple regression is that the model can account for the    combined effect of all predictors and their interactions.
# c) In simple regression, each predictor is treated independently, so it doesn’t capture the full impact of the other variables.
# d) TV and Radio ad budgets are strong predictors of sales, while Newspaper ad budget has a relatively weak effect.
# e) The model’s predictions have an average error of about 3.59 dollars, which is acceptable depending on the data context.
# 2.1. Correlation 
#  a) Given these low correlations, the multiple regression model can still work well, as the predictors (TV, Radio, and Newspaper budgets) don’t seem to be strongly collinear. 
#  b) This is why you were able to achieve a relatively high R² value when combining all the variables together in the model—it allows the model to capture the unique contribution of each variable without much interference from multicollinearity.
# 2.2. Checking Multicollinearity
#  VIF < 5 (no multicollinearity)
#  a) The VIF of 1.004611 is very close to 1, which suggests that there is no significant multicollinearity between TV Ad Budget and the other predictors in your model.
#  b) The VIF of 1.144952 for the Radio Ad Budget is still very low, which means there is little to no multicollinearity between Radio Ad Budget and the other predictors.
#  c) Similar to Radio Ad Budget, the VIF for the Newspaper Ad Budget is 1.145187, which is again low. This means that Newspaper Ad Budget is also not highly correlated with the other variables and is unlikely to cause multicollinearity issues in your model.