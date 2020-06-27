# Regression Analysis


## Abstract
This document summarizes the results of different variants of Linear Regression per-
formed on the Boston Housing Dataset. The linear regression models used include Or-
dinary Least Squares ( OLS ) Regression, Ridge Regression and Lasso Regression. It
summarizes the dependency of coefficients of features on the different values of alpha
for Ridge and Lasso Regression. The residual plots are plotted for the given linear re-
gression models. It also includes the training and test errors for the models.

## 1 Dataset


The name for this dataset is simply boston. It has two prototasks: nox, in which the nitrous
oxide level is to be predicted; and price, in which the median value of a home is to be
predicted.We will be predicting the median value of a home. The origin of the boston housing
data is Natural and it contains 506 cases. There are 14 attributes in each case of the dataset.
They are:

1. CRIM - per capita crime rate by town
2. ZN - proportion of residential land zoned for lots over 25,000 sq.ft.
3. INDUS - proportion of non-retail business acres per town.
4. CHAS - Charles River dummy variable (1 if tract bounds river; 0 otherwise)
5. NOX - nitric oxides concentration (parts per 10 million)
6. RM - average number of rooms per dwelling
7. AGE - proportion of owner-occupied units built prior to 1940
8. DIS - weighted distances to five Boston employment centres
9. RAD - index of accessibility to radial highways
10. TAX - full-value property-tax rate per 10,
11. PTRATIO - pupil-teacher ratio by town
12. B - 1000(Bk− 0. 63 )^2 where Bk is the proportion of blacks by town
13. LSTAT - lower status of the population
14. MEDV - Median value of owner-occupied homes in 1000’s



Figure 1: (a)OLS Regression coefficients for different features.(b)Ridge Regression coeffi-
cients for different values of alpha.(c)Lasso Regression coefficients for different values of
alpha.

## 2 Ordinary Least Squares Regressor

Fitted the OLS regressor and plotted the coefficients for different features. A positive sign
indicates that as the predictor variable increases, the response variable also increases. A neg-
ative sign indicates that as the predictor variable increases, the response variable decreases.
From the plot, it can be seen that the concentration of the nitric oxide has a very high inverse
relation with the price of the house and this is very intuitive too. As the nitric level oxides
concentration increases, the price of the house decreases as it is of less demand.The plot of
coefficients is given in figure 1(a).

## 3 Ridge Regressor

Lambda is used to decrease or regularize the coefficients. After fitting the regressor for
different values of alpha it can be seen that as alpha increases, the coefficients decreased. As
lambda gets larger, the bias is unchanged but the variance drops. Feature with the average
number of rooms decreases the most. The plot for coefficients for different values of alpha
is given in figure 1(b).

## 4 Lasso Regressor

Fitted the lasso regressor on the training dataset and found that as the alpha increases the
coefficients decreases. Lasso shrinks the coefficient estimates towards zero and it has the
effect of setting variables exactly equal to zero when lambda is large enough while ridge
does not. A major advantage of the lasso is that it is a combination of both shrinkage and
selection of variables. However, there were only five features here. The plot for coefficients
for different values of alpha is given in figure 1(c).

## 5 Residual Plots

### 5.1 OLS Residual plot

The residuals are randomly dispersed around the horizontal axis suggesting a better fit. How-
ever, it can be seen that the residual plot exhibit some ‘U’ shape means a non-linear model
will be better than a linear one. The residuals plot is given in figure 2(a).



Figure 2: (a)Residual plot for OLS Regressor.(b)Residual plots for Ridge regressor with
value of alpha to be 10,100,200 respectively.(c)Residual plots for Lasso regressor with value
of alpha to be 3,100,200 respectively.

### 5.2 Ridge Residual plot

As the value of alpha increases the residuals get more scattered around the horizontal axis. It
shows that that model is fitting better for higher alpha.The residual plots are given in figure
2(b).

### 5.3 Lasso Residual plot

In this case as the alpha increases, the residuals start forming vertical patterns which suggest
the overfitting of the model. The residual plots are given in figure 2(c).

## 6 Mean Training and Test Errors

### 6.1 OLS Regressor

The mean training error and test error was less than that compared to the Ridge regressor
and Lasso regressor.


### 6.2 Ridge Regressor

The training error is always less than the test error. As the alpha is increased, the training
and test errors also increases.

### 6.3 Lasso Regressor

In this case the situation was different. The training error is always more than the test error.
As the alpha is increased, the training and test errors decreased.


