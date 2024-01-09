# House Prices Regression

This notebook shows the solution of a regression problem using the Ames Housing dataset. 
Data taken from this <a href="https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview">
Kaggle competition </a>.

The work is an example of building a regression model on data containing 
many different types of features.
The work includes all the main stages of building a data processing pipeline, 
including data preparation, feature engineering, handling outliers,
building several ML models, assessing their performance and optimizing hyperparameters.

The data preparation process includes steps such as data cleaning, 
handling missing values, processing categorical features, etc.

The feature engineering phase consists of various mathematical transformations 
of the original features, 
including estimating feature mutual information and filtering by its value, 
normalizing data by logarithmic transformation, filtering correlated features, etc.
Moreover, it also covers creating additional features using k-Means and PCA algorithms.

Cook's distance and DBSCAN are considered to detect outliers. 

As an estimator 4 tree-based ensemble regression models are considered: XGBoost, lightgbm, 
GradientBoostingRegressor and RandomForestRegressor of sklearn library. 
I limited my consideration to models of this type, since, in addition to neural networks, 
they are the most promising for solving regression problems. 
However, it should be noted that tree-based models are not sensitive to data preparation, 
feature engineering, and naturally incorporate outlier detection. 
Because of this, all the steps above are presented here primarily to illustrate skills 
and do not reveal a significant impact on the regression performance.

At the final stage, the hyperparameters of the models under study are tuned 
using the Optuna package.

# **Authors**
- [Anton Fedarenka](https://github.com/anton-fedarenka)