# MechaCar_Statistical_Analysis

## Overview of the analysis:
A few weeks after starting his new role, Jeremy is approached by upper management about a special project. AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

## What data analytics will be done:
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
- Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## What You're Creating
This new assignment consists of three technical analysis deliverables and a proposal for further statistical study. You’ll submit the following:

- Deliverable 1: Linear Regression to Predict MPG
- Deliverable 2: Summary Statistics on Suspension Coils
- Deliverable 3: T-Test on Suspension Coils
- Deliverable 4: Design a Study Comparing the MechaCar to the Competition

## Resources
- Software: Git version 2.33.0.windows.2, Visual Studio 1.62.2, RStudio RStudio 2021.09.2+382 "Ghost Orchid" Release (fc9e217980ee9320126e33cdf334d4f4e105dc4f, 2022-01-04) for Windows

## Deliverables:
### Linear Regression to Predict MPG
- Mechacar File was uploaded using library function.
![1Mechacaruploades](https://github.com/Jcreye75/MechaCar_Statistical_Analysis/blob/054bf15ca73f5efd72b9405955ff347e907c707d/Resources/1Mechacaruploades.png)

- Linear regression was run using de lm function. 
![2LineaRegression](https://github.com/Jcreye75/MechaCar_Statistical_Analysis/blob/054bf15ca73f5efd72b9405955ff347e907c707d/Resources/2LineaRegression.png)

- P Value and r-squared value was obtained using summary function-
![p-valuer-squaredvalue](https://github.com/Jcreye75/MechaCar_Statistical_Analysis/blob/054bf15ca73f5efd72b9405955ff347e907c707d/Resources/p-valuer-squaredvalue.png)

1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

- mpg: Result: 5.08 e-08 is less than 5% then NON-RANDOM AMOUNT OF VARIANCE
- vehicle_length: Result: 2.60 e-12 is less than 5% then NON-RANDOM AMOUNT OF VARIANCE
- vehicle_weight: Result: 0.07776 is greater than 5% then RANDOM AMOUNT OF VARIANCE
- spoiler_angle: Result: 0.3069 is greater than 5% then RANDOM AMOUNT OF VARIANCE
- ground_clearance: Result: 5.21 e-08 is less than 5% then NON-RANDOM AMOUNT OF VARIANCE
- AWD: Result: 0.1852 is greater than 5% then RANDOM AMOUNT OF VARIANCE

2. Is the slope of the linear model considered to be zero? Why or why not?

Considering the Estimates, linear model would be:

mpg = -0.01040 + 6.267(vehicle_length)+ 0.001245(vehicle_weight)+ 0.06877(spoiler_angle)+ 3.546(ground_clearance)- 3.411(AWD)

RESULT: NON ZERO FORMULA

3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

Yes it is a model to predict mpg. R-squared is 0.7149 and adjusted R-squared is 0.6825, this means a strong correclation. Maybe considering other variables not in the model can adjust de correlation and be more exactly or less correlative.

## Summary Statistics on Suspension Coils
- Suspension Coils File was imported.
![Suspensioncoilupload](https://github.com/Jcreye75/MechaCar_Statistical_Analysis/blob/d4382d774957eb36f0c14c45dea954f14498e739/Resources/Suspensioncoilupload.png)

- Dataframe using the summarize function to get the mean, median, variance, and standard deviation of the suspension coil’s PSI column.
![Totalsummary](https://github.com/Jcreye75/MechaCar_Statistical_Analysis/blob/d4382d774957eb36f0c14c45dea954f14498e739/Resources/Totalsummary.png)

- Dataframe using the group_by and the summarize functions to group each manufacturing lot by the mean, median, variance, and standard deviation of the suspension coil’s PSI column.
![Lotsummary](https://github.com/Jcreye75/MechaCar_Statistical_Analysis/blob/d4382d774957eb36f0c14c45dea954f14498e739/Resources/Lotsummary.png)


1. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

The variance of suspension coils does not exceed 100, the result is 62.29. One relevant consideration, the total variance does not exceed, but if you review each Lot (third picture above), Lot 3 shows a variance of 170, whivh exceed expected 100 pounds. then then per loyt we can assume that Lot 1 and Lot 2 meet desing specifications, but Lot 3 does not. 

## T-Tests on Suspension Coils

1. T-Tests on Suspension Coils All Lots

- Assuming our significance level was the common 0.05 percent, our P-value = 1 is above our significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis, and we would state that the two means are statistically similar.
- Mean - within the within the 95% confidence interval.

![TotalTest](https://github.com/Jcreye75/MechaCar_Statistical_Analysis/blob/5b37c31ead0ab9af4955e6b792bf3bdce9992b96/Resources/TotalTest.png)


2. T-Tests on Suspension Coils Lot 1

- Assuming our significance level was the common 0.05 percent, our P-value = 1.568 e-11 is below our significance level. Therefore, we have sufficient evidence to reject the null hypothesis, and we would state that the two means are no-statistically similar.
- Mean - within the within the 95% confidence interval.

![TestLot1](https://github.com/Jcreye75/MechaCar_Statistical_Analysis/blob/5b37c31ead0ab9af4955e6b792bf3bdce9992b96/Resources/TestLot1.png)

3. T-Tests on Suspension Coils Lot 2

- Assuming our significance level was the common 0.05 percent, our P-value = 0.0005911 is below our significance level. Therefore, we have sufficient evidence to reject the null hypothesis, and we would state that the two means are no-statistically similar.
- Mean - within the within the 95% confidence interval.

![TestLot2](https://github.com/Jcreye75/MechaCar_Statistical_Analysis/blob/5b37c31ead0ab9af4955e6b792bf3bdce9992b96/Resources/TestLot2.png)

4. T-Tests on Suspension Coils Lot 3

- Assuming our significance level was the common 0.05 percent, our P-value = 0.15 is above our significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis, and we would state that the two means are statistically similar.
- Mean - within the within the 95% confidence interval.

![TestLot3](https://github.com/Jcreye75/MechaCar_Statistical_Analysis/blob/5b37c31ead0ab9af4955e6b792bf3bdce9992b96/Resources/TestLot3.png)


## Study Design: MechaCar vs Competition

### Short descprition of a statistical
MechaCar can be compared with its competitor’s using other metrics as follows:
- cost,
- city fuel efficiency,
- highway fuel efficiency,
- horsepower, 
- maintenance cost, 
- safety rating,
- color,
- stole ratio per state.

1. What metric or metrics are you going to test?   
I would test cost, city fuel efficiency, highway fuel efficiency and maintenance cost which are the mainly concerns when a customer get a car.

2. What is the null hypothesis or alternative hypothesis?    
- The null hypothesis is: mean of cost is zero. 
- The alternative hypothesis is: mean of cost is not zero.

3. What statistical test would you use to test the hypothesis? And why?     
I wouold use linear regression summary, in order to obtain cost ratios for competitors and prove the Mechacar is cheaper then others.

4. What data is needed to run the statistical test?     
Obtain at least 33 observations per each competitors car in order to have statistical information and the run statistic on RStudio to obtain comparisons.

Regards

JC