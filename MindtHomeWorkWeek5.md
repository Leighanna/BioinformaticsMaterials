1. What is the mean and standard deviation for Gestation in `mammals`? Include your code and comments.

```
#mean gestation period
mean(mammals$Gestation)
#diverting na
mean(mammals$Gestation, na.rm = TRUE)
```

mean(mammals$Gestation, na.rm = TRUE)
[1] 142.3534
The mean for gestation period is 142.3534

```
#standard deviation
sd(mammals$Gestation, na.rm = TRUE)
```
The standard deviation for the gestation period of animals is: 146.805

2. Write your own function called "convertPercent" to convert from a decimal to percentage. Include your code and comments.

```
#writing a function
convertPercent <- function(x) x*100
```

```
 convertPercent(.75)
[1] 75
```

3. Use a t-test to determine if male and female possums differ in total length using the dataset `possum`. Include your code, comments, and conclusion for the test.

```
#possum length
t.test(totalL ~ sex, data = possum)
```

```
Welch Two Sample t-test

data:  totalL by sex
t = 1.6497, df = 92.609, p-value = 0.1024
alternative hypothesis: true difference in means is not equal to 0
95 percent confidence interval:
 -0.2843695  3.0753721
sample estimates:
mean in group f mean in group m 
       87.90698        86.51148 
```

The t-test showed that the p value is greater than .05 (it is 0.1024) which means that the statistical information is not significant.

4. Use a chi-square test to determine whether mature mothers are more likely to have premie babies using the dataset `ncbirths`. Include your code, comments, and conclusion for the test.

```
#chi square test
ncbirths
#format contingency table
tbl <- table(ncbirths$mature, ncbirths$premie)
#perform chisquare
chisq.test(tbl)
```

```
	Pearson's Chi-squared test with Yates' continuity
	correction

data:  tbl
X-squared = 0.3881, df = 1, p-value = 0.5333
```
The p=value is 0.5333 it accepts the null hypothesis because there is no statistical significance showing mature mothers are more likely to have premie babies.

5. Use ANOVA to determine whether weights of chicks differ by feed type using the dataset `chickwts`. Include your code, comments, and conclusion for the test.

```
#fitting model to one-way ANOVA
fit <- aov(weight ~ feed, data = chickwts )
#results summary
summary(fit)
```

```
              Df Sum Sq Mean Sq F value   Pr(>F)    
feed         5 231129   46226   15.37 5.94e-10 ***
Residuals   65 195556    3009                     
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1
```

The p value is less than .05 which means we reject the null hypothesis. There is a difference in the mean which interprets it as the feed type does affect their weight!



6. How long did it take you to complete these questions?

a little over an hour


7. Extra credit (10 points): If you attended Dr. Pigliucci's Darwin Day keynote address on Thursday evening, describe one example each of science and pseudoscience he discussed.


8. Type SUBMIT as the answer to this question when you are ready for this assignment to be graded.

SUBMIT!!!!!!!!!!!!!!!!!
