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
The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.

For the total population, the variance in PSI for suspension coils is a bit more than 62 PSI, which is within the design specifications.

<img width="335" alt="total_summary" src="https://user-images.githubusercontent.com/100387078/173199220-4df31911-3d52-4fd4-a001-0cdda2140611.png">

Within the total population are 3 manufacturing lots of suspension coils. The variance for Lots 1 and 2 are 0.99 PSI and 7.45 PSI, respectively, which is within the design specifications. However, the variance in manufacturing Lot 3 is more than 170 PSI, which is well beyond the design specification and indicates a manufacturing defect may have occurred for that lot.

<img width="491" alt="lot_summary" src="https://user-images.githubusercontent.com/100387078/173199649-48cc4fd1-0b48-4dc1-8275-ee37beab9de5.png">

## T-Tests on Suspension Coils

### Population, Mu = 1500 PSI


<img width="427" alt="ttest_pop" src="https://user-images.githubusercontent.com/100387078/173199676-12ea1f6a-32fc-4728-a780-960b483e8428.png">

### Manufacturing Lot 1


<img width="806" alt="ttest_lot1" src="https://user-images.githubusercontent.com/100387078/173199682-e56a0737-53d4-4aae-a05e-e9638507f8c8.png">

### Manufacturing Lot 2


<img width="801" alt="ttest_lot2" src="https://user-images.githubusercontent.com/100387078/173199699-084b3e5f-9c37-4b1f-b904-a109aabd5697.png">

### Manufacturing Lot 3


<img width="802" alt="ttest_lot3" src="https://user-images.githubusercontent.com/100387078/173199704-ca30af87-20f8-4f05-8e01-f3f7d8d313b8.png">

## Study Design: MechaCar vs Competition



