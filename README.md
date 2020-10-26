# House Prices Advanced Regression Techniques

Ever wonder how houses are priced? Market forces work to reduce divergences between housing prices. However, sometimes, the process gets inefficient due to lack of speed in information circulation and inaccuracies in estimations. Using regression techniques to price the houses aim to address this issue. In this notebook, I aim to provide an example of how we can apply regression techniques to such a problem, end-to-end, Using EDA and feature engineering for building our model.
## Project Overview
* Created number of models that estimates House Prices to help customers get their dream house with accurate price.
* Exploratory Data Analysis: 
  * Ensuring Approximate Normality of dependent variable.
  * Dealing with Outliers.
  * Exploring Correlations.
* Imputed missing values thre are over 80 features(columns) in dataset, which makes it a mammoth task. Features are Imputed by following:
  * Median.
  * Mode.
  * Manual functions.
* Worked on Feature engineering containing:
  * Numerical variables.
  * Categorical variables.
  * Ordinal variables.
  * Other variables.
* Feature Scaling
  * Due to the presence of outliers, used sklearn's RobustScaler since it is not affected by outliers.
* Used sklearn Pipelines since they sequentially apply a list of transforms and a final estimator. Pipelines can be saved as pkl file for ease of access. It simpifies training code and improves readability.
* Models used are:
  * RidgeCV model.
  * LassoCV model.
  * ElasticNetCV model.
  * Xgboost model.
* Stacking
  * Stacking involves building a metamodel, that weighs our models' predictions together, to give our final predictions, used StackingCVRegressor for greater stability of results.
* Blending
  * Blending involves taking simple/weighted averages of our predictions to give our final predictions.


