## Chapter 6 Multiple Linear Regression


**First Order Model with 2 Predictors**

First order model contains predictor variables with a maximum power of 1. Therefore, the response variable Y is linear in both X1 and X2.

With 2 predictor the response output or the linear regression function is a plane. The E(Y) will fall on the plane define by the regression equation and the errors are the difference between the actual
value of Y and E(Y).

In multiple regression the regression function is usual called regression surface or response surface. 

**Meaning of Regression Coefficients**

In 2 predictor variable linear regression, β0 is the value of Y when X1 and X2 are 0. Hence, β0 has any significance only when X1 and X2 contain 0 in their distribution.

β1 is the mean change in Y with respect X1 when X2 held constant. 

When effect of X1 doesnt depend on level of X2 and vice versa the 2 predictor variables are said to have additive effects or they dont interact.

So first order regression models must have variables that dont interact.

The parameters β1 and β2 are called partial regression coefficients because they reflect partial effect of one predictor variable when the other variable is held constant.


**First Order Model with more that 2 Predictors**


In this setup we have p-1 predictor variables  and the regression equation can be written as:
				E(Y)  = β0 +  β1xi1 + ... βp-1 x1p-1 + ε
				

This response function is a hyperplane with p-1 dimensions. All the assumptions that we have made in 2 predictor approach hold. No interactions, partial effects etc.

**Generalized Linear Regression Model**


				Yi = ∑βiXi + ε where X0 = 1
				
				
Qualitative Predictor Variables:

When X2 variable takes only 2 values 0,1 the regression equation:
			E{Y} = β0 + β1 X1 + β2 X2 
			
becomes:
			E{Y} = β0 + β1 X1  when X2 = 0  and
			E{Y} = β0 + β1 X1 + β2 when X2 =1 
			
So the regression coefficient β2 captures the difference in behavior because of that particular qualitative factor.


Polynomial Regression:

A special case of generalized linear regression that contains higher order terms to make the response function curvilinear.
				
			E{Y} = β0 + β1 X1 + β2 X1^2
			
			which can be re-written as 
			
			E{Y} = β0 + β1 X1 + β2 X2 where X2 = X1^2


Transformed Variables:

We can transform the Y variable also to make the relationship linear with respect to the transformed variable:
			for ex:
			
			logYi = β0 + β1 Xi1 + β2 Xi2 + εi

is one such transformation



Interaction effects:

When the independent variables are not additive the regression because of interactions can be modelled as:

			Yi = β0 + β1 Xi1 + β2 Xi2 + β3 Xi1Xi2 + εi
			
			

Meaning of Linear in Generalized Linear Regression:

It is evident from most of the above examples that Linear Regression models are not restricted to Linear surfaces. The term linear in the linear model
refers to the model being linear in parameters it doesnt refer to shape of response surface.


### Generalized Linear Regression Model in Matrix Terms

			Y = Xβ + ε
			
			where Y is a nx1 vector with Yi being the value of Y for a combination of X 
			
			X is a nxp matrix where xi1 to xip are observations capture in observation i
			
			ε ~ N(0,σ^2) is a nx1 matrix with errors for each observation i 
			
			β is a px1 matrix with parameters for each of x variables containing partial regression relationship between xi and Y.


			
The parameters β can be estimated by 

			 b = 	Inverse(Transpose(X)X)(Transpose(X)) Y
			 
			 

### Analysis of Variance


SSTO - Variance in Y  ∑ (Yi -Ybar)^2

					Transpose(Y) Y - (1/n) Transpose(Y) J Y
					
					where J is an identity matrix of nxn
					

SSE - Variance in Error terms ∑ei^2

				Transpose(e)e
				
				= Transpose(Y- XB) (Y-XB) = Transpose(Y) (1-H) Y
				where H is X Inverse(Transpose(X)X)(Transpose(X))
				
				
SSR - Variance between Yhat and Y bar

			Transpose(Y) (H - (1/n)J) Y
			
			
MSR - Mean Square of Regression
			
			SSR/(p-1) where 1 degree of freedom is lost due to mean Ybar
			

MSE - Mean Square of Errors

			SSE/ n-p where p degrees of freedom are lost because of estimation of p β parameters.
			
			

**F Test for Regression Relation**

In the case of multiple linear regression the F test test for all the coefficients at once

					H0 = β1 = β2 = ..βp = 0
					Ha = not all of (β1 , βp) are 0
					
					
					F* = MSR/MSE


				If F* <= F(1-α;p-1;n-p) dont reject H0
				If F* >  F(1-α;p-1;n-p) reject H0