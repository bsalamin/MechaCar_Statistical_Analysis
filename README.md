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
The t-test for all manufacturing lots combined produced a p-value of 0.06, which is greater than the threshold of 0.05 needed to accept the alternative hypothesis. So, we fail to reject the null hypothesis that the mean PSI of the combined manufacturing lots is significantly different than 1500 PSI.

The test for each manufacturing lot produced p-values of 1 and 0.607 for lots 1 and 2, respectively. Again, we fail to reject the null hypothesis that the mean PSI for manufacturing lots are different than the population mean of 1500 PSI.

However, the t-test for manufacturing lot 3 produced a p-value of 0.0416, which is less than our confidence level of 0.05, meaning we reject the null hypothesis and accept the alternative hypothesis: the mean suspension coil PSI in manufacturing lot 3 is statistically different than the population mean of 1500 PSI. 

### All Manufacturing Lots

<img width="405" alt="ttest_pop" src="https://user-images.githubusercontent.com/100387078/173249909-bced93c6-1a3c-45ec-a2ba-97a7ddeb9051.png">

### Manufacturing Lots

<img width="652" alt="ttest_lots" src="https://user-images.githubusercontent.com/100387078/173249916-a38047fb-df69-4cb1-b2c6-ac95fa04580b.png">

## Study Design: MechaCar vs Competition

In a statistical study to compare performance of the MechaCar vehicles against performance of vehicles from other manufacturers, we would quantify how the MechaCar performs against the competition in areas like cost-to-own, city/highway/combined fuel efficiency, horsepower and torque, maintenance cost, and safety rating.

**Metrics:**
* Manufacturer's Suggested Retail Price (MSRP)
* Cost-to-own (maintenance costs, taxes and fees, insurance rates)
* Power (hp) and torque (lb-ft)
* Fuel efficieny (EPA ratings for city/highway/combined)
* Safety rating (NHTSA)
* Depreciation (3 and 5 yr average resale values)

**Null hypothesis and alternative hypothesis:**

The null hypothesis would be that MechaCar vehicles does not differ from the population mean of the above metrics for competitors' vehicles. The alternative hypothesis would be that the metrics for MechaCar vehicles, on average, have a statistically significant difference from other manufacturers' vehicles.

**Statistical test:**

A multiple linear regression would be used in order to determine correlation and outcome predictability amongst the various factors that indicated MechaCar vehicle's safety, quality, economy, and performance against the competition from other manufacturers.

**Data:**

Data would need to be sourced from MechaCar and its competitors on factors like price, vehicle type/design and performance, as well as other parties like the EPA (fuel efficiency), the NHTSA (safety ratings), and third-party car dealers (depreciation/residual value of used vehicles).



