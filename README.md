# Analyzing marketing promotion campaign <br> ANOVA test + post hoc ANOVA 


## <span style='color:purple' >  **Introduction** <span/>

* In this project, we will work with historical marketing promotion data. We will use the data to run a one-way ANOVA and a post hoc ANOVA test.
<br>
* We will **perform analysis of variance** (commonly called ANOVA) is a group of statistical techniques that test the difference of means among three or more groups.
<br>
* In the dataset, each row corresponds to an independent marketing promotion, where the business uses TV, social media, radio, and influencer promotions to increase sales.
<br>
* Stakeholders want to know if **sales are significantly different among various TV and influencer promotion types** .
<br>
* To address this request, a one-way ANOVA test will enable us to determine if there is a statistically significant difference in sales among groups. 



### This project included:
* Using plots and descriptive statistics to select a categorical independent variable
* Creating and fitting a linear regression model with the selected categorical independent variable
* Checking model assumptions
* Performing and interpreting a one-way ANOVA test
* Comparing pairs of groups using an ANOVA post hoc test
* Interpreting model outputs and communicating the results to nontechnical stakeholders




### <span style='color:navy'> Model Summary: <span/>
    
1. The $R^{2} = 0.874$ means, the model explains  87.4% of the variation in Sales. This makes the model an effective predictor of Sales. <br>  
2. According to the model, Sales with a Medium or Low TV category are lower on average than Sales with a High TV category. For example, the model predicts that a Low TV promotion would be 208.813 (in millions of dollars) lower in Sales on average than a High TV promotion. <br> 
3. The p-value for all coefficients is  0.00 , meaning all coefficients are statistically significant at  p=0.05 <br> 
4. The 95% confidence intervals for each coefficient should be reported when presenting results to stakeholders. For instance, there is a  95% chance the interval  [−215.353,−202.274]


   ## <span style='color:darkblue'> Perform a one-way ANOVA test <span/>
Running a one-way ANOVA test to determine 
whether there is a statistically significant difference in `Sales` among groups. 


* The null hypothesis is that there is no difference in Sales based on the TV promotion budget. The alternative hypothesis is that there is a difference in Sales based on the TV promotion budget.
* Because the p-value is less than 0.05, we would reject the null hypothesis.
* There is a statistically significant difference in Sales among TV groups.

## <span style='color:darkblue'> Perform an ANOVA post hoc test <span/>
Since we have significant results from the one-way ANOVA test, we can apply ANOVA post hoc tests such as the Tukey’s HSD post hoc test.

We would like to compare if there is a significant difference between each pair of categories for TV.


* The first row, which compares the High and Low TV groups, indicates that we can reject the null hypothesis that there is no significant difference between the Sales of these two groups.
* The results were that Sales is not the same between any pair of TV groups.




## <span style='color:darkblue'> Business insights: <span/>

* High TV promotion budgets result in significantly more sales than both medium and low TV promotion budgets. Medium TV promotion budgets result in significantly more sales than low TV promotion budgets.
 
* Estimated difference between the mean sales resulting from High and Low TV promotions: $208.81 million (with 95% confidence that the exact value for this difference is between 200.99 and 216.64 million dollars).

* Estimated difference between the mean sales resulting from High and Medium TV promotions: $101.51 million (with 95% confidence that the exact value for this difference is between 93.69 and 109.32 million dollars).
difference between the mean sales resulting from Medium and Low TV promotions: 107.31 million (with 95% confidence that the exact value for this difference is between 99.71 and 114.91 million dollars).

* The linear regression model estimating Sales from TV had an R-squared of 0.871, making it a fairly accurate estimator. The model showed a statistically significant relationship between the TV promotion budget and Sales.

* The results of the one-way ANOVA test indicate that the null hypothesis that there is no difference in Sales based on the TV promotion budget can be rejected. Through the ANOVA post hoc test, a significant difference between all pairs of TV promotions was found.
