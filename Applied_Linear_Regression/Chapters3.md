## Chapter 3 Diagnostics and Remedial Measures

Linear Regression is a parametric model where we make assumptions about the data and error terms.
We need to test for these assumptions before we make any conclusions from the fitted regression model.

### Diagnostics for the Predictor Variable

We need to check for the distribution of X for any outliers. 

To do this we can simply plot the distribution of x on a dot plot. Dot plot is useful when the number of samples is smaller.
It provides a visual view of the distribution of x and also if there are any outliers we need to treat for.

Another plot which might not be useful in all cases is a sequence plot. This is to understand if there is any trend in the sequences like time, location or organizations.

The stem and leaf plot is identifying a 10s digit as the stem and all the values in the range of that 10s digit to be its leaves. It provides and indication of frequence 
of each decile of numbers and helps validate normality visually. It also help understand, the mode in the decile band.

Box plot is another excellent visual approach to identify outliers in the data.

### Residuals 

Residual is defined as:
				ei = Yi - Yhati
				
The residual capture the difference between predicted and actual values of Y.

**Properties of Residuals**

Mean: Mean of residuals is 0

Variance: The variance of n residuals is MSE 

Non independence:  The residuals are not independent because they involve Yhati which uses the same regression function. Hence residuals have 2 constraints ∑ei=0
Similarly, ∑Xiei=0

Any departure on the below conditions can be evalated by residuals: 

1. The regression function is not linear
2. Error terms dont have constant variance.
3. Error terms are not independent.
4. The model fits all but one of fewer outlier observations.
5. The errors terms are not normality
6. One or several predictor variables are omitted from the model.


**Diagnostics of Residuals**

The informal approach to gather information on the 6 types of departures mentioned above are:

1. Plot of residuals against predictor variable.
2. Plot of absolute or squared residuals against predictor variable.
3. Plot of residuals against fitted values.
4. Plot of residuals against time or otl1er sequence.
5. Plots of residuals against omitted predictor variables.
6. Box plot of residuals.
7. Normal probability plot of residuals


Non linearity of regression function:

Residual plot against the predictor variable or residual plot against the predicted value provides a much better understanding on the linearity of the regression function.

If there is a pattern in the residual values wrt the predictor variables it indicates that the linear regression line is not sufficient.

Non constancy of error variance:

Plotting residuals or absolute values of residuals or square residuals against the predictor variables gives us if the residuals variance is constant or if it has a relationship
with Y.

If any of these residual plots show some trend it indicates that the linearity assumption doesnt hold and we would need to see other approches to finding the regression function.


Presence of Outliers:
Outliers can be identified either by residual plots against predictor variables or predicted values. Box plots, Stem and Leaf Plot and Dot plots also help us in identifying these
outliers.
As a rule of thumb any value falling 4 standard deviations away from mean of the distribution can be treated as an outlier.
Outliers can be ignored if we cant explain the variation or determine the cause of the variation.

Non independence in error terms:

If there is a trend in the error terms that are collected through time or between locations that are close to each other. This is a problem because this indicate that there is some
relationship between time and the predicted variable and hence must be adjusted.

Normality of Error terms:
A histogram or dot plot will help us identify any distinct departure from normality of error terms.

The other approach is to estimate the error standard deviation and calculate the percentage of observations in 1 2 and 3 standard devations and if they follow the estimates of normal distribution.

Normal Probability Plot:
This is a plot between the residual and the expected value of the residual under normality assumption. Any significant deviation from a straight line indicates devations from normal distribution.

Omitted Variables:
We have to plot the distribution of errors against omitted variables to evaluate if the omitted variables have some information to provide about the Y variable.

### Tests to evaluate residuals

**Test for Randomness**

Two test that we could use to check for randomness are:

1. Runs test: Here positive and negative can be the 2 symbols and we calculate the run metric and decide if the distribution is random or not.

2. Durbin-Watson Test: This is a test to identify any serial correlation between the error terms and hence also is a test for randomness.


**Tests for Constancy of Variance**

1. Rank correlation between predictor variables and residuals: This test measure if there is a relationship between X and error terms.

2. Brown-Forsythe Test: This test to to measure if the variance of the errors is constant or not.

It is robust to non normality assumption, it means that we can infer the test statistic at a significance level even when the errors are not normally distributed.

The test consists of the following steps:

1. Order the errors in the order of errors for the specific predictor variable in the increasing order 

For ex: if e1, e2, e3 are errors for x1, x2 and x3 respectively and x2> x1 > x3. Then the order of the errors would be e3,e1,e2

Divide the errors into 2 groups g1, g2 with n1 and n2 terms which are equal to n terms in the overall dataset.

Calculate the deviation from median of the error term in their respective groups

				di1 = |ei1 - e~1|
				di2 = |ei2 - e~2|
				

Calculate  the mean of the deviations from each of the distributions

			d1bar = mean(di1)
			d2bar = mean(di2)
			

The t statistic for the test is:
			t*bf = (d1bar-d2bar)/s (sqrt(1/n1) +sqrt(1/n2))
			
Where 
			s = (∑(di1 - d1bar)^2 + ∑(di2 - d2bar)^2)/(n-2)
			
The statistic follows a t distribution with n-2 degrees of freedom.  The higher values indicate that the variance of errors is not constant.


3. Breusch-Pagan Test: This test is a large sample test and assumes that  error terms are normally distributed and the variance for error term εi is σi2.

The other assumption is that the variance is related to X with the following relation:
				 log(σi2) = γ0 + γ1Xi
				 

This implies that variance of increase or decreases with X depending on the sign of γ1.

The test is a Chi-square test with the null hypothesis that γ1 =0

The test statistic is :
				
				𝜒2BP = (SSR/2)/(SSE/n)2
				
where SSR is the regression sum of square regression error terms on X. and SSE is the error sum of square regression Y on X.



**Tests for Outliers**

The simplest test is to build a regression line using n-1 non suspect observations and estimate the probability that the observation occurs from this regression line.
If the probability is significantly low we can discard the outlier value

**Test for Normality**

1. Chi-square Test
2. Kolmogorov-Smirnov Test
3. Lilliefors Test


### Correlation test for Normality of residuals

By calculating the correlation coefficient 	between the residuals ei and their expected values from normal distribution and testing for the correlation coefficient value for a given α
will determine if the errors are normally distributed or not.


The other test for normality of residuals is Shapiro-Wilk test that can be approximately viewed as correlation coefficient between ordered residuals and their expected values under normality


### F test for lack of fit

This test is to measure if the regression function adequately fits the data.

The assumptions for this method are:

1. Observations Y for a given X are independent
2. Observations Y are normally distributed
3. Have constant variance σ2

For F test for lack of fit we would need multiple samples for Y and X at the same level of X. These repeat samples are called replicates and the repeat trials are called
replications.

asumming we have 5 levels of X then n1,n2,n3,n4,n5 will be the total number of replicates of each value of X and the sum will be n the number of observations.


Yij is the ith observation for the jth level of X

Yibar is the mean of all the Y values for a particular level of X.

Full Model

				Yij = μj + εij
				
				where 
				μj are parameters for 1 to c
				εij are independent N(0,σ2)
				
Since error terms mean is 0

				E(Yij) = μj


Now coming to the test statistic:
				SSE(F)  = ∑∑(Yij - Ybarj)^2 ==SSPE
		
		In the context of test for lack of fit, it is call Sum of Squares of Pure error.
		
		The degrees of freedom would be n-p where p is the number of levels of X
		
		
Reduced Model:

The null hypothesis would be that the linear regression is valid 

Using this assumption the variables for test statistic are calculated as follows:

			SSE(R) = ∑∑ (Yij - Yhatij)
			
It is sum over prediction for a value of Xj across multiple repicates captured.
			
The degrees of freedom would n-2 where n is the total observations.
			

The test statistic is given by:
			
			F* = 	((SSE(R) - SSE(F))/ dfR -dfF)/ (SSE(F)/dfF)
			

ANOVA Table:

We can extend the normal ANOVA table to now capture
		SSR = ∑∑(Yhatij -Ybar)^2
		
		SSE = ∑∑(Yij - Yhatij)^2
		
		SSLF = ∑∑ (Ybarj - Yhatij)^2
		
		SSPE = ∑∑( Yij -Ybarj)^2
		
		SSTO == ∑∑(Yij - Ybar)^2
		
		

**Box Cox Transformation**


The approach is to automatically make the relationship between transformed Y and X as linear as possible.

it involves regression

			Y^λ = β0 + β1x + ε
			
The method to estimate lambda is either by a linear search of λ that maximizes the MLE or directly using the MLE estimate of Y and X with λ also as a parameter.


### Method to identify shape of the Regression Linear

**Lowess Method** Locally weighted regression scatter plot smoothing

The approach is the calculate multiple regression equations in the neighbourhood determined and keep doing this in a rolling window approach.

To smoothen these lines:
1. To give lesser weights to weights far away from a given target x a lesser weight.

2. To adjust for outliers, the observations that contributed for higher first iteration error will be given lesser weight in iteration 2.

3. To improve robustness Step 2 is run iterative and updating the weights.


The smoothened curve along with the confidence interval of the fitted regression line can be used to imply confidence in the developed regreesion model.


				


