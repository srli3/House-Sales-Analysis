# House-Sales-Analysis


#### Introduction

 For decades, house sale price forecasting has always been a hot topic. Unlike macroeconomists who make predictions of the housing market according to the economic situation, people usually would estimate the price of a certain house based on variables such as the size, location, and condition of the house. For this project, I decided to build models on house prices in order to investigate how internal and external factors would influence the sale price. I chose a dataset published on Kaggle in 2016 <https://www.kaggle.com/harlfoxem/housesalesprediction>. This dataset includes house sale prices for King County in Washington between May 2014 and May 2015. It’s scraped from KingCounty.gov with the dimension of 21 columns and 216,213 rows. Among 21 columns, there only exits one variable(date) that is not numerical, which suggests this data would be a good choice for building regression models based on it.

#### Findings

##### Location Matters
Location, Location, Location. Most people heard this mantra about the price of properties. In project, this saying is confirmed by comparing two models’ ability of prediction. While model 1 utilizes variables of house size and location,  reduced model 2 only uses house size-related variables. As expected, model 1 shows great improvement than model 2 by explaining 16.75% more about the variation of data (greater R-squared).

##### Polynomial Model Wins
Within this project, I built 2 multiple regression models and 2 polynomial models with degrees of 2. After conducting ANOVA test and comparing R-squared values between them, I conclude that polynomial models outperform the multiple regression ones. The best model achieved R-squared value of 0.8082.

##### Bigger House, More Expensive per Sqft
How house price is influenced with the increase in size? Will bigger house be cheaper per sqft? I conducted two proportion comparison of this assumption. Opposite to what I expected, data shows house with greater number of bedrooms or larger lot size both result in higher price per sqft. However, I believe this conclusion might be influenced by the type of property, and testing on apartment sale instead of house sale could give a different answer.

