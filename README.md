# MechaCar Statistical Analysis
Statistics in R and RStudio

The following statistical analysis utilizes R and RStudio to accomplish the following:
* Load, clean up, and reshape datasets using tidyverse in R.
* Visualize datasets with basic plots such as line, bar, and scatter plots using ggplot2.
* Generate and interpret more complex plots such as boxplots and heatmaps using ggplot2.
* Plot and identify distribution characteristics of a given dataset.
* Formulate null and alternative hypothesis tests for a given data problem.
* Implement and evaluate simple linear regression and multiple linear regression models for a given dataset.
* Implement and evaluate the one-sample t-Tests, two-sample t-Tests, and analysis of variance (ANOVA) models for a given dataset.
* Implement and evaluate a chi-squared test for a given dataset.
* Identify key characteristics of A/B and A/A testing.
* Determine the most appropriate statistical test for a given hypothesis and dataset.


## Linear Regression to Predict MPG
In the linear regression to predict miles-per-gallon, it is safe to assume the population fits a normal distribution: the min and max are similar |-19.47| and |18.58| and the median -.07 is near zero.

At the 95% confidence level, vehicle length and ground clearance have statistically significant, non-random amounts of variance. Vehicle weight, spoiler angle, and AWD have p-values greater than 0.05 and are not statistically significant at this confidence level. The p-value for the intercept is also less than 0.05, indicating there are other factors that affect MPG that are not explained in this analysis.

With a p-value of 5.35e-11, the slope can be inferred as non-zero.

The R-squared value of 0.7149 means that this linear model predicts mpg of MechaCar prototypes effectively 71.49% of the time. There are other factors not captured here that also affect MPG.

<img width="817" alt="summary_lm" src="https://user-images.githubusercontent.com/100387078/173194269-f1bdafb9-f550-4e13-9b47-6c70a160ba50.png">

## Summary Statistics on Suspension Coils


## T-Tests on Suspension Coils

### Population, Mu = 1500 PSI

### Manufacturing Lot 1


### Manufacturing Lot 2


### Manufacturing Lot 3



## Study Design: MechaCar vs Competition
