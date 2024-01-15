# Regression Analysis Examples

Detailed implementation of various regression analysis models and concepts on real dataset.  

### Regression Models Covered
* Simple Linear Regression Model
* Multiple Linear Regression Model
* Count Based Dataset Regression Models - Poisson, Negative Binomial, Generalised Poisson
* Quantile Regression Model
* Ordinary Least Squares (OLS) Estimate Based Regression Model
* Generalised Least Squares (GLS) Estimate Based Regression Model

### Regression Concepts Covered
You will find implementation of below concepts which can be used for your reference:
* Log Returns
* Ordinary Least Squares (OLS) Estimate
* Generalised Least Squares (GLS) Estimate
* MultiCollinearity
* Variance Inflation Factor (VIF)
* Standardized Residuals
* Studentized Residuals
* Leverages
* Outliers
* Influential Cases
* Cook's Distance
* Regression Diagnostics
* Residual Diagnostics
* Feature Engineering
* Goodness of Fit - Deviance and Pearson Chi-Squared
* Regression Parameters Significant Tests
* Heteroskedasticity
* White's Heteroskedasticity Consistent (HC) Estimator
* Heteroskedasticity & Autocorrelation Consistent (HAC) Estimator
* Q-Q Plot
* LOESS smoothed estimate
* AutoCorrelation
* Simple Linear Regression Model
* Multiple Linear Regression Model
* Poisson Regression Model
* Binomial Regression Model
* Generalised Poisson Regression Model
* Quantile Regression Model

### General Regression Analysis Steps
(It's overall guidance not strict, only for overview)
1. Load Dataset
2. Visualise dataset (if possible)
3. Feature Engineering (if required)
4. Define Regression Model
   * Response variable (y)
   * Explanatory variables or features (X)
   * Residual assumption (start with Gauss Markov Assumption)
5. Feature Selection
   * check for MultiCollinearity and take action
   * Apply PCA 
   
   Goal: features should be independent
6. Fit Regression Model (starts with OLS Estimate)
7. Regression Diagnostics
   * Regression parameters significance using t-test & generalised linear F-Test.
   * Leverages, Outliers and Influential cases
   * R-Squared 
   * For Count based dataset, goodness of fit (Deviance and Pearson Chi-Squared)
   
   Goal: All regression parameters are statistically significant, High R-Squared, 
   model shouldn't be affected by influential cases.
8. Residual Diagnostics
   * Plots:
     * Residual plot only
     * Residual vs fitted values
     * Q-Q plot
     * ACF plot
   * Tests:
     * Homoskedasticity
     * Normal Distribution
     * Auto-Correlation 
   
   Goal: Residual should be white noise.
9. If required delete influential cases, modify model in terms of explanatory 
   variables and | or residual assumption. Go to 6-7-8 step again.
10. Once we have satisfied model, do forecasting + performance metrics on test dataset.