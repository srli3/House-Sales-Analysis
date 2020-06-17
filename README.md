# House-Sales-Analysis
Analysis of House Sales in King County, USA



Prediction of House Sale Price in King County


Introduction

For decades, house sale price forecasting has always been a hot topic. Unlike macroeconomists who make predictions of the housing market according to the economic situation, people usually would estimate the price of a certain house based on variables such as the size, location, and condition of the house. For my project, I decided to build models on house prices in order to investigate how internal and external factors would influence the sale price. I chose a dataset published on Kaggle in 2016. This dataset includes house sale prices for King County in Washington between May 2014 and May 2015. It’s scraped from KingCounty.gov with the dimension of 21 columns and 216,213 rows. Among 21 columns, there only exits one variable(date) that is not numerical, which suggests this data would be a good choice for building regression models based on it.

Findings

Location Matters
Location, Location, Location. Most people heard this mantra about the price of properties. In my project, I confirmed this saying by comparing two models’ ability of prediction. While model 1 utilizes variables of house size and location,  reduced model 2 only uses house size-related variables. As I expected, model 1 shows great improvement than model 2 by explaining 16.75% more about the variation of data (greater R-squared).

Polynomial Model Wins
Within this project, I built 2 multiple regression models and 2 polynomial models with degrees of 2. After conducting ANOVA test and comparing R-squared values between them, I conclude that polynomial models outperform the multiple regression ones. The best model achieved R-squared value of 0.8082.

Bigger House, More Expensive per Sqft
How house price is influenced with the increase in size? Will bigger house be cheaper per sqft? I conducted two proportion comparison of this assumption. Opposite to what I expected, data shows house with greater number of bedrooms or larger lot size both result in higher price per sqft. However, I believe this conclusion might be influenced by the type of property, and testing on apartment sale instead of house sale could give a different answer.

Summary

At first, I created a histogram plot of all variables. We can see some of the variables are close to normal distribution. Furthermore, I did log-transformation for dependent variable price and size-related variables for model building. For model fitting, I built multiple regression models and polynomial models accordingly. Since the polynomial models with the highest R-squared value, we can say that this model successfully explains 80.82% variation of price.

Histogram of  Variables & Log-transformation
 

Multiple Regression Model:
   

Polynomial Regression Model:
 
For proportion comparison, I created 2 tables for testing. Both result in p-value of 1 which suggests there is strong evidence that greater number of bedroom ( > median of the number of bedroom) and larger lot size ( > median of the log(lot_sqft)) will bring expensive price per sqft ( > median of the price per sqft). 
    

In addition, I tried a test case of predicting the price of a 2b2b house built in 2016 in Bellevue, Seattle. The predicted price is $602,082.7 with the 95% confidence interval range from $382,151.9 to $947,585.1. Searched real house price in Bellevue, I found this outcome is not accurate. If we want to forecast current house price, data should be updated since house sale price is quite time-sensitive.
















Reference

Data schema from https://www.slideshare.net/PawanShivhare1/predicting-king-county-house-prices

