## Chapter 7 Multiple Regression II

### Extra Sum of Squares

Extra sum of squares is the reduction in SSE due to the addition of a new predictor variable into the model given that a set of variables or a variable is already in the model.
It could also mean marginal increase in SSR due to the addition of the new predictor variable given the exisiting variables in the model.

The order of addition of the variables into to the model is important because it determines the SSR and SSE of the initial model.

Also, since SSTO = SSR + SSE extra sum of squares can be calculated by both the below approaches:
			
				 SSR(X2| X1) = SSR( X1,X2) - SSR(X1) = SSE(X1) - SSE(X1, X2) 
				 
The above formula is intuitive because the decrease in SSE because of addition of X2 must be equal to SSR because of adding X2. The matching will happen because SSTO the total sum of squares will be constant for the data.

This gives us a set of formulas:
				
				 SSR(X3 | X1, X2) = SSE(X1, X2) - SSE(X1, X2, X3) = SSR(X1, X2, X3 ) - SSR(X1,X2)
				 
				 SSR( X3, X2 | X1 ) = SSE(X1) - SSE(X1,X2,X3) = SSR( X1, X2, X3) - SSR(X1)
				 
				 SSR(X2 | X1 )  <> SSR(X1 | X2)
				 
				 
**Decomposition of Extra Sum of Squares**


We start the decomposition with a series of steps:
				
				SSTO = SSE(X1) + SSR(X1)
				
					 = SSR(X1) + SSR(X2|X1) + SSE(X1,X2)
					 

We also know for a fact that 

				SSTO = SSR(X1,X2) + SSE(X1,X2)
				
				
Solving for both of them:
				
				SSR(X1,X2) = SSR(X1) + SSR(X2|X1) = SSR(X2) + SSR(X1|X2)
				
				

We can also extend this to multiple values of X like this
				
				SSR(X1,X2,X3) = SSR(X1) + SSR(X2|X1) + SSR(X3 | X1,X2) = SSR(X1) + SSR(X2,X3 |X1)
				
				
				
				
Anova table can then be further broken down into MSR added by each additional variable.

### Uses of Extra Sum of Squares in Tests for Regression Coefficients

** Test whether a single βk can be dropped from the multiple regression model **

				H0:  βk = 0
				Ha:  βk <> 0
				
				
The test statistic wil be:
				
				t* = bk/ s{bk}
				
				
				
The other alternative approach using ANOVA table would be:

				F* = ESS(Xk) / SSE(Full Model)
				
				   =   ((SSE(X1..XK-1) - SSE(X1..XK))/((n-k+2) - n-k-1) ) / SSE(X1..XK)/n-k-1
					
				   =  	((SSE(X1..XK-1)-SSE(X1..XK)/1)/SSE(X1..XK)/n-k-1)
				   
				   
		
** Test whether several βk are 0 **

					H0: β2 = β3 =0
					Ha: β2 or β3 <> 0
					
					
Using the variation in SSR of mulitple variables 


				F*  = ((SSE(X1) - SSE(X1,X2,X3))/2 )/ SSE(X1,X2,X3)/n-4


### Summary of Tests Concerning Regression Coefficients


Test whether all βk =0

				
				F* = SSR( X1...Xp-1)/p-1  / SSE(x1...xp-1)/n-p
				
					

Test whether a particular βk =0

				F* = ESS(xk) /SSE(Full Model)
				

Test whether some βks are 0

				F* = ESS(xk..xk+p)/ SSE(Full Model)
				
				

### Coefficients of Partial Determination

Similar to R-square which measures the proportionate reduction in variation of Y because of the variables in the model.

Coefficient of Partial Determination measures the marginal decrease in variation because of adding a variable X.


**Two Predictor Variables**

For a 2 predictor variable model 

Relative marginal reduction in variation in Y associated with adding X2 given X1 is already in the model is:

				SSR(X2|X1)/SSE(X1) == (SSE(X1) - SSE(X1,X2)) / SSE(X1)
				

**General Case**

The generalization of coefficients of partial determination would be:

				Rsquare Y4 | X1,X2,X3 = SSR(X4|X1,X2,X3)/ SSE(X1,X2,X3)
				

Essential what percentange of the error of the exisiting model is explained by adding the variable X4.


**Coefficient of Partial Correlation**

Square root of Coefficient of Partial Determination is Coefficient of Partial Correlation.


### Standardized Multiple Regression Model

Standardized for of general mulitple regression models control for round off errors in normal equations and permit comparision of estimated regression coefficients
in common units.


** Round of Errors in Normal Equation Calculations**

Round off errors occur when  Transpose(X)X calcuation occurs and when Det(X) is calculated. If Det(X) is a very small number then the round of errors have very serious consequences.
Similarly if Transpose(X)X has variables that vary significantly in values then round off error is difference is prominent.

The solution is to transform the variables and reparameterize them to Standardized Regression Model.

The transformation is called **Correlation Transformation** that makes all the entries in the Transpose(X)X matrix vary between -1 and 1. This makes the calculation 
of the inverse matrix less a subject of round off errors.


**Lack of Comparability in Regression Coefficients**

Regression coefficients in unstandardized model cant be compared because of the difference of units involved.

This is very obvious when the units of 2 variables are on different scales that are not comparable.

**Correlation Transformation**

Correlation transformation involves centering and scaling the variables which means:
				
				(Y- Ybar)/s(Y)
				
				
**Standardized Regression Model**

Standardized Regression Model equation would look like
				
				Yi* = β1* Xi1* +...+ βp-1* Xip-1* + εi
				
				
The intercept in Standardized regression model will always be 0 because MLE or Least Squares Approach would have the parameter be 0.

The intuitive explanation is that since all the variables are standardized and intercept explains the value of Y when all the input X's are 0. The value of Y must be 0 because 
Y is also standardized. Because, all Xs are 0 when they are at their mean and and the same is removed from Y and hence the intercept would be 0.


### Muticollinearity and its Effects


When predictor variables are correlated among themselves then intercorrelation or multicollinearity is said to exist among the variables.


** Uncorrelated Predictor Variables**

When uncorelated predictor variables are used no matter the order in which they are introduced into the model the ESS reduction would be their marginal contribution.

Also, because of this their coefficient no matter the order or existence of the other variables will be the same.


** Perfectly Correlated Predictor Variables**

When 2 variables are perfectly correlated, the space spanned by the variables falls into a lower dimension and hence we would get mulitple solutions to the same data.

Essentially, what we are fitting is a line and many planes can have that line in their region. Hence, there is no way for us to explain which of the response functions
 is the best fit for the data.
 
 Also, it does not mean that we cannot arrive at a good fit for the Regression Model.
 
	
**Effects of Muticollinearity**

The implications are:
1. The correlation between the predictor variables doesnt mean that we cant obtain a good fit for regression equation or does it affect the inteferences in the region in which the model was built.
Essentially, the region where the X variables were used to build the model.

2. The assumption in the regression models is that β coefficients measure mean increase in Y for unit increase in X holding all the others constant, which is not possible in collinear variables.
Thus when collinear variables are included the regression coefficient represents marginal contribution of variable after all the correlated variables contribution in the model.


** Effect on Extra Sum of Squares**

Highly correlated variables have very minimal ESS because they both contribute to the explanation of same variation in the data.


**Effect on s{bk} **

As more correlated variables are add the variability in the estimates of the regression coefficients s{bk} increases significantly.


**Effect on Fitted Values nad Predictions **

As long as the interpretation is among the fitted values or in the fitted region, the regression equation holds. However, interpretation in the region outside is not adviced because multiple planes can have a line that can be a part of the planes.


**Effect on Simultaneous test of βk**

When we use the t statistic to measure the Bonferroni estimate of regression equation holding both correlated variables and their estimates β1 and β2.

We have to check the value of t* = bk/ s{bk} at 0.9875 because of 2 variables.

Because both the variable are correlated which cause the variation in s{b1} and s{b2} we would not reject that β1 and β2 are 0.

But a F Statistic test that includes both the variables 

						F* = (SSR/2)/(SSE/n-3) 
						
would reject the null hypothesis that  both β1 and β2 are 0 because the additional information from SSR(X2|X1) will be less both SSR(X1) is significant enough to establish relation between Y and X1 or X2.


Hence we must be carefull choosing the test when using correlated variables