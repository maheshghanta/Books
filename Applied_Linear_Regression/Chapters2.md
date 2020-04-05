## Chapter 2 Inferences in Regression and Correlation Analysis

### Inferences concerning β1

β1 is the linear relationship between the dependent and the independent variable. So, for any hypothesis test:

H0: β1 = 0
Ha: β1 <> 0

So for rejecting the null hypothesis we must come up with a distribution for b1 the estimate of β1. 

#### Sampling distribution for b1

E{b1} = β1

σ2{b1) = σ2/∑(Xi- Xbar)^2

where σ2 is the variance of Y

This gives us the unbiased estimator for β1 and the variance of the estimator.

This can be used to estimate β1 and confidence in the estimate.

Since we assume b1 is normally distributed, the sampling distribution  (b1-β1)/s{b1} the standard statistic will be used to make inferences about β1.

The students t-test is used to compare if there is a statistical difference between the estimate β1 and b1.


The test statistic:
				(b1-β1)/s{b1} is distributed as t(n-2) for the regression model
				
				
The loss of 2 degrees of freedom is because of the estimates β0 and β1 which are estimated from the data.


**Confidence interval for β1**

Since  (bl - β1)/s{b1} follows a t distribution, we can make the following probability
statement:
				P{t(α/2;n-2) <= (b1 - β1)/s{1}  <= s t(l - α/2;n - 2)} = 1 - α 
				
				
Using this we can arrive at the confidence interval for β1. This is:

				bl ± t(l - α/2; n - 2)s{b1}
				

**Test with respect to β1**

Since (b1-β1)/s{b1} is distributed as t with n - 2 degrees of freedom. Using t distribution, the tests we could do are:

2 sided test: to test if there is a linear relationship between dependent and independent variable
where H0: β1 =0 and Ha: β1 <> 0 will be the hypothesis test


1 sided test: to test the sign of the coeffiecient.

where H0: β1 > 0 and Ha: β1<=0 will have rejection of null hypothesis if the t test value <= t(1-α, n-2) because α is only in 1 direction.
Similarly, H0: β1 < 0 and Ha: β1>=0 will have rejection of null hypothesis if the t test value >= t(1-α, n-2) because α is only in 1 direction.

###  Inferences concerning β0

Using the equation  b0 = Ybar - b1 \* Xbar

the mean and variance of b0 are given by:

				E{bo}  = β0
				s2(b0} = σ2 \[1/n + Xbar2/∑(X-Xbar)2\]


Using the same t distribution as estimates of b1, the interval estimate of b0 is:

				b0 ± t(l - α/2; n - 2)s{b0}

**Power of a test**
It is the probability of rejecting NULL hypothesis when its false.	
				Power = P{|t\*| > t(1- α/2;n - 2)|(β1 - βest)/ s(b1)}
				
Essentially, we are estimating what is the probability of avoiding type 2 error. Not rejecting null hypothesis when we have to.


### Confidence band for regression line

We can also inference the confidence interval for the regression line.

The approach to get the confidence interval for the regression line involve a test called Working-Hotelling test.

The confidence interval for any value Xh is  Yhath +/- W\*s{Yhath)
where:
					W2 = 2F(1-α;2;n-2)
					
### ANOVA analysis of Regression Analysis

		SSTO = (Yi - Ybar)^2
		
		It is a measure of total variance in the data
		
		SSE = (Yi- Yhati)^2
		
		It is a measure of total error made by the regression model
		
		SSR = (Yhati - Ybar)^2
		
		it it the total variance explained by the regression line.
		
		SSTO = SSR + SSE
		
		
		Degrees of freedom would be
		
		SSTO has n-1 degrees of freedom because ybar removes 1 degree of freedom
		
		SSR has 1 degree of freedom because Yhat has 2 degrees of freedom β1 and β0. One degree of freedom is lost by sum(Yhati - Ybar) must be 0
		
		SSE has n-2 degrees of freedom where 2 degrees of freedom are lost by β1 and β0. 
		
		
		Using ANOVA table we can establish if β1=0 or not.

The Test used is F Test and the statistic F is:

					F = MSR/ MSE
					
					where MSR = SSR/ degrees of freedom of SSR
					
					MSE = SSE/  n-1-degrees of free of SSR
					
	

### Measures of Linear association between X and Y

**Coefficient of Determination**

				R2  = SSR/SSTO = 1 -SSE/SSTO
				
**Limitations of R2**

1. High value of R2 does not mean that we can make a confident prediction of Y because it depends of variation in epsilon.

2. High value of R2 does not mean that the relationship is linear. It just implies that there a signification linear component.

3. Low value of R2 again doesnt mean that there is not relationship between Y and X.


**Correlation Coeffient **

One approach is a signed square root of R2

Others are:

Pearson Correlation Coefficient:
				r12  = ∑ (Y1i - Y1bar)(Y2i - Y2bar) / sqrt(\[ ∑(Y1i - Y1bar)2 ∑(Y2i - Y2bar)2])
				
This is a biased estimate of rho12 the correlation between Y1 and Y2.


The t test statistic to establish correlation would be: 

				t\* = r12 sqrt(n-2)/sqrt(1-r12^2)


Spearman Rank Correlation:

When the normality assumption on Y1 or Y2 is not valid rank correlation tries for find the monotonic relationship between Y1 and Y2.
				rs  = ∑ (R1i - R1bar)(R2i - R2bar) / sqrt(\[ ∑(R1i - R1bar)2 ∑(R2i - R2bar)2])
				

