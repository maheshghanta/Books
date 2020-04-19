## Chapter 8 Regression Models for Quantitative and Qualitative Predictors

### Polynomial Regression Models

Problems with Polynomial Regression models is extrapolation outside the decision surface is not recommended because the data might turn to other direction outside the decision surface.


**Second Order 1 Variable Regression Model**

					Yi = β0 + β1xi + β2xi^2 + ε
					
					
**Two Predictor Variables Second Order Model**

					Yi = β0 + β1xi1 + β2xi2 + β11xi1^2 + β22xi2^2 + β12xi1xi2 +εi
					
					
The coefficient β12 is called interaction effect coefficient 


**Partial F Test**

The test to check if a first orde model is sufficient is:

					F* = (SSR(x1^2,x2^2,x1x2| x1,x2)/3) /(SSE/n-6)
					


### Interaction Regression Models

A simple and common way of modeling interaction effects is the cross product of 2 variables. For ex. for a 2 variable model β3x1x2 is an interaction term.

The interaction term of simple cross product is called linear by linear or bilinear  interaction term.



** Interpretation of Interaction Regression Models with Linear Effects**


Regression Coefficients Interpretation:

Because of the interaction term now the coefficients become non independent and hence 

				β1 + β3X2 is the change in Y for unit change in X1 when X2 is held constant
				
Similarly
				β2 + β3X1 is the change in Y for unit change in X2 when X1 is held constant
				


When the sign of the interaction coefficient is positive for a fixed value of X2 the  increase in Y when X1 is variable is positive. Similarly, for X2. 

Hence, we would say that the interaction effect is synergetic or reinforcing


If the interaction coefficient is negative, the variables themselves are of inteference or antagonistic variables.


**Interpretation of Interaction Regression Models with curvilinear effects**

We need to interpret the interaction effect after taking the partial derivative with the variable we would want to vary and then interpret the interaction effect.



**Implementation of Interaction Effects in Curvilinear regression**

As a partial remedy of high multicollinearity center all the X variables.


When the number of variables is large the number of interaction variables will also be large and this will force us to have large datasets before we can model for all interactions.




### Qualitative Predictors

**Qualitative Predictor with 2 levels**

When we have 2 qualitative variables that are mutually exclusive then if we include both the variables in the model the Transpose(X)X matrix that is used to extract linear
regression relationships becomes non singular and hence we cant estimate the parameters.

Hence, for c level qualitative variable we represent it by c-1 level indicator variables by dropping 1 which will be the case when all the c-1 variables are 0.


**Interpretation of regression coefficients**

Essentially because these variables just indicate the presence or absence of a paricular event/action. The interpretation would be change in the intercept of the regresssion line.


The regression line would be 

				Yi = β0 + β1x1 + β2x2 where x2 is the indicator variable
				
				When x2 =0
				
				Yi = β0 + β1x1
				
				when x2 =1
				
				Yi = (β0 + β2) + β1x1
				
				
Hence, the indicator variable just shifts the regression line by a constant for each class.



### Considerations using Indicator Variables

When having multiple classes encoded as numbers in single variable. The interpretation of the variable indicates that the change in Y because of each of the class would be the same.

This might not be the real case because there is an implicit assumption that the 3 classes are equidistant when we used numbers which might not true representation of the data.

Indicator variables dont make any such assumptions and hence are a more reliable.


### Modelling interactions between Qualitative and Quantitative Variables


The interaction term with indicator variable helps change the slope of the regression function by the presence and absence of the qualitative variable.

The β estimate indicator the change in slope when the variable is present.

Having more than 1 qualitative predictor variables and their interaction terms, taking partial derivative with respect to the variable of interest helps interpret the 
variable.

The test for significance of the interaction term would be:

						H0 : β3 is 0
						
						Ha : β3 <>0
						
						
						F* = (SSR(X1X2| X1,X2)/1 )/ (SSE (X1,X2,X1X2)/n-4)