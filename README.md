# T-test---The-Effects-of-Different-Types-of-Fiscal-Spending-on-Different-Economies
## Overview of Project
We chose to look at 5 countries for our study. Those countries are France, Turkey, India, the United Kingdom(UK), the United States (US). We chose these countries in part because we wanted a fairly diverse group of countries. But in order to conduct a complete analysis, we needed large amounts of public information on each country’s economies. Those two factors determined our five countries. We also decided to use recent data, from the years 2011 to 2015. 

### Purpose
To test the effects of different types of fiscal spending on different economies. 
The unit for time is years, and the unit for GDPPC is the US dollar. The unit for GDPPC_C is the percentage change in GDPPC.


### Dataset:
![Untitled](https://user-images.githubusercontent.com/38533045/163076572-100ba846-6284-4be8-a14f-eead2c5fd505.png)


The data provided is from a set of 5 countries during 5 common years. The data was collected through the website https://countryeconomy.com/ along with data from https://datacommons.org/ 


## Analysis 
We will predict the effect that federal spending composition has on GDPPC. This will be achieved through the following predictor variables: 

Defense (Defense spending as a percentage of total fiscal expense);

Education (Education spending as a percentage of total fiscal expense);

Health (Health spending as a percentage of total fiscal expense).

Our Response variable is GDPPC_C (Percent change in GDPPC).

In order to determine which predictor variables have an effect on GDPPC and which don’t, we will use simple linear regression models as well as multiple regression models.

Results and Discussions
Choosing which variables to assess
Three models will be assessed. One from Backward Elimination, one from Forward Selection, one from all subsets. All calculations will use AIC. If a model is already being assessed the second best will be used.

Backward Elimination: Model 1: GDPPC_C = Defense

Forward Selection: Model 2: GDPPC_ = Defense + Education

All Subsets: Model 3: GDPPC_ = Defense + Health

### Fitting and assessing GDPPC_C vs. Defense
![Untitled2](https://user-images.githubusercontent.com/38533045/163076843-543df829-8b8a-43c9-b9ff-eb7bd878a522.png)


The simple linear regression model for this relationship is:
GDPPC_C = .765(Defense) - .047

This means for every 1% increase in defense spending as a percent of total fiscal spending GDPPC_C will increase by .0076%. This minuscule increase is not surprising given the weakness and low amplitude shown by the plot. To determine whether or not the relationship between GDPPC_C and Defense is statistically significant, we should consider the relationship at a 95% significance level.

The p-value of the coefficient Defense is .0481, just barely below the .05 significance level. This would indicate that the relationship between Defense and GDPPC_C is statistically significant. While just barely passing the statistically significant metric, the adjusted r^2 value is .1228. This indicates that about 12.28% of the variance in GDPPC_C can be explained by Defense spending. This is terrible news for this model as that indicates that the vast majority of the variance is properly described by variables other than Defense.

### Fitting and assessing GDPPC_C vs. Defense + Education


The Multiple Regression Model for this relationship is:
GDPPC_C = .719(Defense) + .155(Education) - .063

This means for every 1% increase in defense spending as a percent of total fiscal spending GDPPC_C will increase by .0072%. For every 1% increase in education spending as a percent of total fiscal spending, GDPPC will increase by .0016%. To determine whether or not the relationship between GDPPC_C and Defense & Education is statistically significant, we should consider the relationship at a 95% significance level.

The p-value of the coefficient Defense is .130, which is above the .05 significance level. This would indicate that the relationship between Defense and GDPPC_C is not statistically significant. 

The p-value of the coefficient Education is .864, which is above the .05 significance level. This would indicate that the relationship between Education and GDPPC_C is not statistically significant. 

The adjustedR2value did not improve over Model 1. The adjusted R2is .0842. This indicates that about 8.42% of the variance in GDPPC_C can be explained by Defense spending and Education spending. This is terrible news for this model as that indicates that the vast majority of the variance is properly described by variables other than Defense or Education.

### Fitting and assessing GDPPC_C vs. Education + Health


The Multiple Regression Model for this relationship is:
GDPPC_C = .746(Defense) - .101(Health) - .032

This means for every 1% increase in defense spending as a percent of total fiscal spending GDPPC will increase by .0075%. For every 1% increase in education spending as a percent of total fiscal spending, GDPPC will increase by .0010%. To determine whether or not the relationship between GDPPC_C and Defense & Health is statistically significant, we should consider the relationship at a 95% significance level.

The p-value of the coefficient Defense is .0582, which is above the .05 significance level. This would indicate that the relationship between Defense and GDPPC_C is not statistically significant. 

The p-value of the coefficient Health is .586, which is above the .05 significance level. This would indicate that the relationship between Education and GDPPC_C is not statistically significant. 

The adjusted R2value did improve over Model 4. The adjusted R2is .0955. This indicates that about 9.55% of the variance in GDPPC_C can be explained by Defense spending and Health spending. This is terrible news for this model as that indicates that the vast majority of the variance is properly described by variables other than Defense or Health.

Picking the Best Model
After testing multiple different models on the basis of AIC the best model was model1. GDPPC_C = 1 + Defense. This model was chosen because of the following reasons:

Model 1 had the lowest AIC value.
Model 1 had the highest adjusted R2value of the models tested.
Model 1 is statistically significant because the p-value is less than .05

Analyzing the Best Model
Model 1: GDPPC_C = .765(Defense) - .047 is the best model for this data.










After viewing the assumption plots we can see that the points are fairly spread out. We can see that the normal Q-Q plot is fairly linear and positive. This means that our results are normal. We already know that independence has been violated.

### Conclusion
After testing all of the data, it is clear that the data given in Model1 is the best indicator of GDPPC_C. Education and Height never were significant variables. Given that Defense was the only significant variable and the fact that Defense only accounted for 12.28% of the variance in model1 would incline us to believe that a proper model for predicting the change in growth of GDPPC_C would be beyond the scope of the variables we considered in this study. GDPPC_C growth is incredibly complex, and involves dozens of variables we didn’t consider in this assessment.
