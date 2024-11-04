1.	Analysis 1: 

a)	Research Question: 
Is there a statistically significant linear relationship between age and feelings of life among Canadian adults?

b)	Variables
Independent Variable: DEMO_age (Continuous Variable represents the age of each independent person)

Dependent Variable: WELLNESS_life_satisfaction (Discreate Variable, each independent person’s feeling of life generally on a scale from 0-10, each age is paired to a wellness of life, assume the Independence of Observations)

c)	Visualization
Scatterplot with Regression Line: The research question is about linear regression, so a scatterplot would be sufficient to show the correlation between variables and potential outliers. A regression line will be added to the plot to visualize the linear trend between the two variables.

d)	Analysis Method
The population size is about 11428, missing rows will be first removed(assume the missing data is not bigger than 5% of the population size). In addition, 570 randomly selected samples(5% of the population, to make precise result) will be used to form a scatterplot with a regression line and value of coeficient correlation r.

To test the statistical significance of the correlation coefficient, a hypothesis test will be conducted to determine the extent of rejecting the null hypothesis.

Null Hypothesis ($H_0$): There is no linear relationship between age and feelings of life in the population of Canadian adults.
Alternative Hypothesis ($H_A$): There is a linear relationship between age and feelings of life in the population of Canadian adults.

Bootstrap: Randomly resample paired age and feelings of life data again and again(500 times) with replacement and calculate the r value for each bootstrapped sample. Then create a bootstrapped sample distribution and find the p-value(based on a significance level of 0.05) and make the conclusion for this hypothesis.




2.	Analysis 2

a)	Research Question: 
Is there a statistically significant association between age group (young adult, adult, older adult) and the frequency of reported feelings of isolation (NA, Some of the time, Hardly Ever, Often)?

b)  Variables
Independent Variable: DEMO_age (nominal categorical variable with three levels: young adult (<30), adult (30 ≤ x ≤ 60), and older adult (>60))

Dependent Variable: LONELY_ucla_loneliness_scale_isolated (categorical variable that represents how isolated each person feels from others, categorized as NA, Some of the time, Hardly Ever, Often)

c)	Visualization
Boxplots will be used to visualize the distribution of people's feelings about isolation for young adult, adult, and older adult groups. This will provide a visual comparison of central tendency (mean, median, interquartile range, outliers) and spread of the scores for each group.

d) Analysis Method:
Hypothesis test:
($H_0$)It is hypothesized that there will be no association between age group and isolation levels. 

(#H_1#)It is anticipated there will be no association between age group and isolation levels, and specificlly, older adults might report experiencing isolation 'Often' at a higher frequency than younger adults, given potential age-related factors such as retirement, loss of social connections, and health challenges.

Chi-Squared Test of Independence:

To test if there is a statistically significant association between two categorical variables, a chi-squared test of independence will be used because my research question seeks to determine whether there is a statistically significant association between age group and feelings of isolation, rather than differences in means or distributions. 570 samples in total (190 samples for each age group) will be randomly selected to create a contingency table that cross-tabulates the observed frequencies of each combination of age group and isolation level. Assumptions include sample independence, where the isolation level of one individual does not influence another's. Expected frequencies will be calculated, and a chi-squared test statistic will be computed at a 0.05 significance level to determine if any observed patterns differ significantly between age groups.


Analysis 3:

a)  Research Question:
"Is there a statistically significant difference in the proportion of older adults and others who have been diagnosed with back pain?"

b)  Variables:
Independent Variable: DEMO_age (categorized into "older adult(>60)" and others(≤60)).

Dependent Variable: WELLNESS_backpain_diagnosis (binary: "Yes" or "No").

c)  Visualization
Histogram of Bootstrapped Differences: This plot provides a visual representation of the sampling distribution of the difference in proportions obtained through bootstrapping. The histogram would display the frequency of different bootstrapped differences, allowing you to assess the shape and spread of the distribution.

d)  Analysis Method:
Bootstrapped Confidence Interval for the Difference in Proportions:

To estimate the range of plausible values for the difference in back pain diagnosis proportions between ages, a bootstrapped confidence interval for the difference in proportions can be used. 

This method involves, first, subsetting the data to include only younger adults(≤60) and older adults(>60), and then calculating the proportion of individuals diagnosed with back pain within each age group. Next, bootstrapping is performed for a specified number of iterations (e.g 10,000), during which samples are randomly selected with replacement from each age group to create bootstrap samples, and the difference in back pain diagnosis proportions between the bootstrap samples is calculated. Using the distribution of bootstrapped differences, the 2.5th and 97.5th percentiles are then calculated to construct a 95% confidence interval. Finally, the confidence interval is interpreted. If it includes 0, there is no statistically significant difference in back pain diagnosis proportions between the two groups, while if it does not include 0, there is evidence of a statistically significant difference.

PS: It is anticipated that older adults may have a higher proportion of back pain diagnoses, the confidence interval will give the answer of how confidence we can assume this hypothesis is true.


```python

```
