# House Prices Advanced Regression Techniques

Ever wonder how houses are priced? Market forces work to reduce divergences between housing prices. However, sometimes, the process gets inefficient due to lack of speed in information circulation and inaccuracies in estimations. Using regression techniques to price the houses aim to address this issue. In this notebook, I aim to provide an example of how we can apply regression techniques to such a problem, end-to-end, Using EDA and feature engineering for building our model.

# Project Overview
* Created number of advanced regression models that estimates House Prices to help customers get their dream house with accurate price.

# Exploratory Data Analysis: 

## Ensuring Approximate Normality of dependent variable.

![](https://github.com/sarvaatmak/House-Prices-Advanced-Regression-Techniques/blob/main/images/norm1.png)

## Dealing with Outliers.
![](https://github.com/sarvaatmak/House-Prices-Advanced-Regression-Techniques/blob/main/images/outliers.png)
### After Outliers are tweaked using log.
![](https://github.com/sarvaatmak/House-Prices-Advanced-Regression-Techniques/blob/main/images/norm2.png)

## Exploring Correlations.

![](https://github.com/sarvaatmak/House-Prices-Advanced-Regression-Techniques/blob/main/images/correlations.png)

# Imputed missing values:
![](https://github.com/sarvaatmak/House-Prices-Advanced-Regression-Techniques/blob/main/images/missing.png)
## There are over 80 features(columns) in dataset, which makes it a mammoth task. Features are Imputed by following:
* **Median.**
* **Mode.**
* **Manual functions.**

# Worked on Feature engineering of:
* **Numerical variables.**
* **Categorical variables.**
* **Ordinal variables.**
* **Other variables.**

# Feature Scaling
  * **Due to the presence of outliers, used sklearn's RobustScaler since it is not affected by outliers.**

#### Used sklearn Pipelines since they sequentially apply a list of transforms and a final estimator. Pipelines can be saved as pkl file for ease of access. It simpifies training code and improves readability.

# Models used are:
* **RidgeCV model.**
![](https://github.com/sarvaatmak/House-Prices-Advanced-Regression-Techniques/blob/main/images/ridge_weights_against_alphas.png)
* **LassoCV model.**
* **ElasticNetCV model.**
* **Xgboost model.**

# Stacking
* **Stacking involves building a metamodel, that weighs our models' predictions together, to give our final predictions, used StackingCVRegressor for greater stability of results.**

# Blending
* **Blending involves taking simple/weighted averages of our predictions to give our final predictions.**

# Model performance
* **Ridge Regression Cross Validation Score: -0.020624477100858817**

* **Lasso Cross Validation Score: -0.025771379440506597**

* **ElasticNet Cross Validation Score: -0.0211354966632166**

* **XGB Regression Cross Validation Score: -0.01687074227172932**

* **LGB Regression Cross Validation Score: -0.01603367673085801**
### Here we can conclude that Light Grading boosting has Cross Validation Score: -0.01603367673085801 which is lowest compared to all other models .

## Finally saved the predictions to csv files.
