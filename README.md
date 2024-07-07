# Housing-Project
Build predictive models to estimate housing prices based off of various factors.

Portfolio Project: House Prices

Objective:
The goal of this analysis is to predict the price of homes based on various features of housing such as number of bedrooms, house area, furnishing, etc. 

Data: The Housing Prices dataset from Kaggle contains 545 observations with 13 features. These features include the median value of homes (target variable) and attributes such as average number of bedrooms, bathrooms, area square footage, etc.

Skills
- R programming 
- Linear Regression model
- Predictive and statistical analysis 
- Visualizations 

Exploratory Analysis (EDA):
1. Data Cleaning 
There were no missing values or nulls in the dataset. There were also no duplicates. 
I checked the data types and found that some of the predicting variables were categorical variables. I converted the categorical data using as.factor()
2. Relationships
EDA revealed that features such as the number of bathrooms and area, had moderate correlations with housing prices. The remaining correlations seem to be moderate to weak. Visualizations included histograms, box plots, and scatter plots to understand the distributions and relationships between variables.
I evaluated the boxplot of each categorical variable against the dependent variable price that showed the medians. 
Created scatterplots to observe the linear relationships between price and each predicting variable. I took note of the trends and direction for each. 
I created  a correlation matrix to check the correlation between the variables. Most of the correlations were weak, with only a few moderately strong correlations between price and the independent variable. I did not observe any high correlations between the predicting variables, suggesting against multicollinearity. 


Analysis:
1. Model Fitting 
Split the data into a training set and testing set. 
I chose to fit the data using Linear regression due to its simplicity and interpretability. The full model included all available features, while the reduced model included only the most significant predictors at alpha 0.01.
I compared the two models using r^22 and the adjusted r^2 value of the two models, and computed rsme and mse.

Findings: 
The P-value of the f-statistic is 2.2e-16, which is less than the alpha level so we can reject the null. Concluding that, the additional predictors in the full model significantly improves the model. 
R^2 is the proportion of variance explained by the predictors. Adj r^2 considers the other variables. The full model has a higher adj r^2 value than the reduced model. It explains 68.3% of the variability in price. That's about 7% more than the reduced model.

3. Outliers & Multicollinearity 
I checked for significant outliers using cook's distance with a threshold of 1, and found no significant outliers. 
I checked for multicollinearity among the predictors using VIF and found that no values exceeded the threshold, therefore no evidence of multicollinearity. 

4. Prediction
Obtained very large rsme and mse values for the prediction model. 
Overall, the full model that includes all of the predictors was able to predict 67% of the variability in the data. It is a better model than the reduced model, by about 7% since it explains more of the variability in price. 
