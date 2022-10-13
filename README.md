# MechaCar_Statistical_Analysis

MechaCar production analysis using R

## Overview

Jeremy with his vast experience and exhausted knowledge of Cars, has been selected as the primary analyst by AutosRUs for retrospective analysis on historical data, analytical verification and validation of current automotive specification and study design of future product testing. Jeremy has to make sure that his analysis contains statistical backbone, quantitative metric and clear interpretation. Based on the results, a proposal will be made on study design, hypothesis and analysis workflow in roder to make manufacturing process even better. We used R, RStudio and tidyverse/deplyr package for analysis.

## Results

###Linear Regression to Predict MPG

MechaCar prototype production is dependent on multiple metrics such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance. A Linear Regression was run to predict the main factors which affects MPG the most. 

![linear model](https://user-images.githubusercontent.com/108366412/195621673-c86a9482-af57-4c16-92a1-be36290ebb0f.png)

![linear model](https://user-images.githubusercontent.com/108366412/195639975-86adbd82-1b71-4807-bd78-b4c523de8668.png)

![regression_lines](https://user-images.githubusercontent.com/108366412/195666471-73ab3bdf-baf2-462b-b767-934fb0a98313.png)

* **Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?**
  Vehicle length with a p-value of 2.60e-12 and Ground clearance with a p-value of 5.21e-08 are the variables/coefficients providing non-random amount of variance in finding mpg values in the dataset. Both these variables are <0.05 
* **Is the slope of the linear model considered to be zero? Why or why not?**
  The slope coefficients of multiple variables -vehicle length, ground clearance, and AWD contain significant non-zero values. Also their p-values are <0.05 (significance level set as 0.05). Hence, the slope of this linear model is not zero. 
* **Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?**
  The linear model does predict the mgg of MechaCar prototypes to a certain extent. The Multiple R^ value is 0.7149 which indicates that there is a correlation between dependent and independent variables. Variables such as ground clearance and vehicle length help in predicting the mpg value. However, there is scope to improve the model by including more significant variables can be included to increase model significance. 
  
### Statistical summary for Suspension Coils

  The statisfical summary of Suspension Coils shows that the mean is 1498.78 and median is 1500. The data has a standard deviation of 7.892627. 
  Variance of the overall data is at 62.29356 which is lower than the set limit of 100 pounds per square inch indicating that the current manufacturing data does meet design specifications for all manufacturing lots in total.
  
![summary_table](https://user-images.githubusercontent.com/108366412/195667188-a7b43839-2481-4cdf-b62e-122cb4a636cc.png)

  Below image shows the mean, median, standard deviation and variance of all 3 lots individually. Variance for lots 1 and 2 are well within the acceptable limit of 100 pounds per square inch however, lot 3 has a variance of 170.2861224. Thus, we can say that Lot 3 does not meet the design specifications.
  
![lot_summary](https://user-images.githubusercontent.com/108366412/195667198-22146cc6-f3d8-40c7-b127-2dffdb7d708f.png)

### T-Tests on Suspension Coils

T-Tests were performed on Suspension Coil data to determine if there was any statistical difference between the population mean of 1500 and the sample mean. From the below image which show the T-Test between the population mean and the total sample mean, it can be inferred that there is no statistical difference between them as p-value stands at 0.06 which is greater than the 0.05 significance level
![t-test_total](https://user-images.githubusercontent.com/108366412/195671280-9a98a6ba-3e14-4448-adc1-070ab0dbc08c.png)

T-Test performed on individual lots showed that lot 1 and 2 with a p-values of 1 and  0.6072 is not statistically different from the population mean. However, lot 3 is having a p-value of 0.04168 suggesting us that the lot 3 mean is significantly different from the population mean.
![t-test_lot](https://user-images.githubusercontent.com/108366412/195671307-f521af83-a3af-4cb9-973a-26d43e88a026.png)

## Study Design: MechaCar vs Competition


