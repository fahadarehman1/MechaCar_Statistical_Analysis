# AutoRUs newest prototype
UW Data Bootcamp - Module 15

- ### **Linear Regression to Predict MPG:** 
  
  ![](C:\Users\Fahad.Rehman\Desktop\UW DataBootcamp\R_Analysis\01_Demo\lm_predict_mpg.PNG)
  
  ![](C:\Users\Fahad.Rehman\Desktop\UW DataBootcamp\R_Analysis\01_Demo\summary_lm.PNG)
  
  - Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
  
    - From the above linear regression analysis we can see that vehicle length and ground clearance are non-random attributes. The p-values for both these attributes resulted in 2.60e-12 and 5.12e-08. 
  
  - Is the slope of the linear model considered to be zero? Why or why not?
  
    - The slope of the linear model is not zero as we can see that p-value for the model is 5.35e-11. This means there is sufficient evidence to reject our null hypothesis. 
  
  - Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
  
    - The r-squared value of the linear model is 0.7149 which means that around 71% of all mpg predictions will be calculated by this model. The linear model does predict mpg of MechaCar prototypes effectively.
  
      
  
- ### Summary Statistics on Suspension Coils

  ![Total Summary](C:\Users\Fahad.Rehman\Desktop\UW DataBootcamp\R_Analysis\01_Demo\total_summary.PNG)                                                   ![Lot Summary](C:\Users\Fahad.Rehman\Desktop\UW DataBootcamp\R_Analysis\01_Demo\lot_summary.PNG)

  - The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
    - As seen from the above data frames(Total Summary and Lot Summary) the overall variance is less than 100 psi(per square inch) and meets the design specification but when we drill down on lot level we can see that lot3 has a variance of 170.286 which is way over the acceptable threshold of 100 psi.
  
  ### T-Tests on Suspension Coils:
  
  - Briefly summarize your interpretation and findings for the t-test results. Include screenshots of the t-test to support your summary.
  

<img src="C:\Users\Fahad.Rehman\Desktop\UW DataBootcamp\R_Analysis\01_Demo\t_test.jpg" style="zoom:75%;" />

- The one sample t-test for everything combined recorded a p-value of 0.061 which is low enough to reject the null hypothesis.
- The sample t-test of **lot 1** yields the p-value of 1 which is significantly higher than standard p-value so the null hypothesis cannot be rejected in this case. Also the population mean is similar to combine result set.
- The sample t-test of **lot 2** yields the p-value of 0.6072 which is higher than standard p-value so the null hypothesis cannot be rejected in this case. Also the population mean is similar to combine result set.
- The sample t-test of **lot 3** yields the p-value of 0.0416 which is low enough to reject the null hypothesis. Also the population mean is similar to combine result set.



## Study Design: MechaCar vs Competition.

1. Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.

   First of all there's no one fit all situation when it comes to buying or evaluating a car. Comparing mpg between a 4 cylinder to 6cyclinder doesn't make sense also comparing a hybrid to electric is a different ball game. There are instances where consumer is willing to sacrifice the mpg to gain the horse power or in some cases off-road capabilities(Jeep Wrangler or Ford Bronco). 

   I would also suggest running an ANOVA test to compare different competitors 

2. In your description, address the following questions:

- What metric or metrics are you going to test?

  - Two metrics that I would like to test are Engine(Gas/Hybrid/Electric) with Price, MPG and Cost of Ownership over the span of 10years

- What is the null hypothesis or alternative hypothesis?

  - Null Hypothesis - Ho : There is no statistical significance between MechaCar and competition

  - Alternate Hypothesis - Ha: There is statistical significance between MachaCar and competition

    *** We can further drill down on different attributes to compare and prove or not prove the null hypothesis based on p-value*

- What statistical test would you use to test the hypothesis? And why?

  - I would suggest running ANOVA as that can compare the means of continuous numerical variables across different attributes.

- What data is needed to run the statistical test?

  - Engines broken down by Gas/Electric and Hybrid. Horse Power of each car, MSRP on each base model, ownership cost(including replacing batteries if needed) and mpg(miles per gallon). I would also look into weather variable as we can't compare data from Wisconsin to data from Texas.

