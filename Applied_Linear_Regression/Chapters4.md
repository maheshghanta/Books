## Chapter 4 Simultaneous Inferences

### Joint estimation of β0 and β1

**Need for joint Estimation**

Typically when we get the interval estimate for β0 and β1. The confidence interval is for each of those parameters separately. 

So the confidence interval for the regression function would be lesser than .95 which will be the confidence interval of one of the parameters.
To arrive at a confidence interval for the regression estimate is difficult because both the parameters are not independent because they are 
estimated from the same data.

When we do any analysis the estimates we provide would have some error but we would want to have an assurance around the set of estimates being correct.
We can call these estimates family of estimates.

This brings us to 2 different confidence coefficients, which are:

1. Statment confidence coefficient: This is the confidence that the estimated parameter for ex.β0 will be within the specified confidence interval even when it is
estimated by taking multiple samples from the population.

2. Family Confidence coefficient: This is the confidence that a family of estimates, incase of simple linear regression (β0 and β0) both of them together are withing the 
specified confidence interval. Essentially, if the confidence interval is 0.95, in 95% of samples β0 and β1 estimates will be correct and in 5% sample either of β0 or β1
will be wrong.

The procedure to construct simultaneous confidence intervals is called Bonferroni procedure.


**Bonferroni Joint Confidence Intervals**

Using an intuitive approach of reducing the confidence interval for each of the estimates makes the confidence interval for the joint distribution better,
we estimate the joint confidence interval.


Lets start with simple probability. Let there be 2 events A1 and A2 which are the events when β0 and β1 are not in the confidence interval of (1-α).

Hence,

				P(A1) = α
				P(A2) = α
				
			
				P(A1 U A2) = P(A1) + P(A2) - P(A1 ∩ A2)
				
				
Next using the complementation property we would arrive at the desired region

				P(A1bar ∩ A2bar) = 1 - P(A1 U A2)
								 = 1 - P(A1)-P(A2) + P(A1 ∩ A2)
								 
								 
Using the fact that P(A1 ∩ A2) is alway greater than or equal to 0, we arrive at
				P(A1bar ∩ A2bar)  >=  1 - P(A1)- P(A2)
								  >=  1 - 2α
								  
								  
Therefore using bonferroni inequality, we can come up with lower bound for confidence of the regression equation give confidence level of individual parameter.

**Simultaneous Estimation of Mean Responses**

The reason why we need family confidence coefficient is that, the combination of sampling errors in b0 and b1 may be such that E(Yh) will be correct for some values of X and wrong for others.


** Working - Hotelling Procedure **

The procedure is based on confidence band for the regression line. The procedure helps find the range of Yh for a value of Xh.
 
We can use the boundary values of Xh to estimate the 1-α boundary values of Yh using the procedure.

					Yhath +/- Ws{Yhath}
					where
					W2 = 2F(1 - α; 2, n - 2)
						

This estimate give a 1-α confidence of the estimate of Yhat and assurance that the procedure leads to all correct estimates in the family of estimates.


** Bonferroni Procedure **

The confidence interval for Yhath from Bonferroni procedure is:

					Yhath +/- Bs{Yhath}
					
					where B = t(1-α/2; n-2)
					
					
### Simultaneous Prediction of Intervals for New Observations
Simultaneous predictions of intervals involves coming up with range of Yhath for g simultaneous samples of X.  Essentially it is 1-α confidence for all the g samples that we are currently estimating.

Two estimation approaches are Scheffe and Bonferroni.
The simultaneous prediction limits for g predictions with Scheffe procedure with family confidence coefficient 1-α are:

				Yhath ± Ss{pred}
				where:
				S2 = gF(1-α;g; n-2)
				
				
With Bonferroni procedure the 1-α limits are:
				Yhath ± Bs{pred}
				B = t(1 - α/2g; n - 2)
				

### Regression through Origin

Regression through origin is estimating the values of Y with only 1 parameter β1 and the assumption that Y when X=0 is 0.

**Caution on Regression through Origin **

The regression through origin will not constrain sum of errors to be 0.

The only constraint is: ∑Xiei=0

Another important point is that the SSE = ∑ (Yi- Yihat)^2 can exceed  ∑(Yi-Ybar)^2. This can occur when the pattern of relationship is curvilinear/linear with intercept value >0.

Hence, the value of R2 will become negative. Therefore, any inference from R2 cant be made from regression through origin.


### Effects of Measurement Errors

Measurement errors are mistakes made in the data collection process.


** Measurement Errors in Y **
Any random measurement errors in Y will not create any problem as long as the errors are uncorrelated and unbiased.

** Measurement Errors in X **

However, the same cant be said incase of measurement errors in X because any error in the estimation of X would make the error terms biased and hence make the regression
equation unstable.


**Berkson Model**

The model assumes that temperature or pressure if fixed at a certain value. However, due to malfunctioning of thermostat the acutal temperature might be a random variable.


However, given that X the thermostat measure is always set to constant the error term εi- β1δi is independent because Xi is always constant.

Because the following conditions are met:
1. The error terms have expectation zero.
2. The predictor variable is a constant, and hence the error terms are not correlated with it.

Normal regression can be executed for Berkson model.


### Inverse Predictions

Xhat can be estimated by observing Yhat by reversing the linear regression equation subject to b1 <>0.

				Xhath(new) = (Yhnew - b0)/b1  
				
The interval estimate of Xhat would be:

			Xhath(new) ± t(l - α/2; n - 2)s{predX}
				
			where:
			
			s2(predx) = MSE/b12 {1 + 1/n + (Xhathnew - Xbar)^2 / ∑(Xi- Xbar)^2}
			
			
			
### Choice of X levels

The key decisions to be made in choice of X variables are:

1. How many levels of X should be investigated?
2. What shall the two extreme levels be?
3. How shall the other levels of X, if any, be spaced?
4. How many observations should be taken at each level of X?


If the main objective of regression equation is to estimate slope β1.  The two extreme levels of X must be sufficient.

However, we are not sure if the line accurately fits the relationship.

If the objective is to estimate  β0 then number of Xs or their location doesnt matter as long as Xbar= 0

General advice given by D.R cox is :

2 levels of X if we want the relationship between predictor variable and dependent variable

3 levels if we want to estimate the curvature of the relationship too

4 levels if we want to further examine the relationship curve.
				