## Effects on Imports and Exports on GDP
Applied a panel data model to understand the effects of imports and exports on GDP across time and different countries
## How It's Made
* Data
  - https://www.kaggle.com/datasets/yasserh/wine-quality-dataset
* Packages
  - plm
  - AER
  - MASS
  - corrplot
  - car
  - ggplot2
  - coefplot

## Key Features
* Descriptive Statistics
  - Boxplots
  - Histograms
  - Scatterplots
  - Correlation plots
* Panel Data Models
  - Pooled Model
  - Fixed Effects
  - Random Effects
* Finding the Best Model
  - Cluster-Robust Standard Errors
  - Plot Means
  - Coefficient Plots
  - pFtest
  - pHtest
## Summary
We run the fixed effects model and compare it to the pooled model. 
To identify the preferred model we ran the pooled model, the fixed effects model, and the random effect model. To compare the pool effects to the fixed effects model, we used the Pftest function. Testing both firm and time effects versus the pooled model, we obtained a low p value meaning that both firm and time effects were better than the pool model. Testing only the time effects against the pooled model, we obtained a p value equal to one. This meant that the time effect was not significantly different. Lastly, testing the firm effects only against the pooled model resulted in a low p value, so the firm fixed effects is the preferred model. 

From these three tests, we can conclude that the fixed effects model including the firm is preferred over the pooled model. To verify these findings, we plotted all of these effects onto a coefficient plot. This plot showed us that none of our betas crossed zero. Next, we compared this to the random effects model. This resulted in a large p-value, so we failed to reject the null hypothesis and concluded that the random effects model was preferred. Given the random effects model using GLS, this is the best model to use out of the three. Plotting the coefficients of the random effects model, the beta values did not cross the insignificance line validating that it is the best model.


