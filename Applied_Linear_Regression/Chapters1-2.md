# Applied Linear Regression

Linear Regression is one of the most important and fundamental statistical techniques anyone who wants to do data analysis must be good at.
This book is one of the comprehensive books that discusses about this technique.
The	book can be bought from here [Amazon](https://www.amazon.in/Applied-Linear-Regression-Probability-Statistics/dp/1118386086/ref=dp_ob_title_bk)


## Chapter 1 Linear Regression with One Predictor Variable

The book starts by discussing functional and statistical relationship between variables.

**Functional Relationship** Any mathematical formula that ties 2 sets of variables is a functional relationship. For ex: 
				*y = f(x)*
Has y as the dependent variable and x as the independent variable

All functional relationships are certain i.e they always foloow the functional relationship.

**Statistical Relationship** Unlike functional relationships which are deterministic or definitely follow the relationship, statistical relationships do not 
necessarily fall on the curve of relationship.

Regression model is a formal way of expressing essential ingredients of statistical relationships:
1. Tendency of dependent variable *y* to vary with any independent variable *x* in a systematic fashion.
2. The scattering of the dependent and independent points around the line of relationship.

In simplistic terms, the relationship between the independent and dependent terms and distribution of errors is defined by regression model.

These 2 characterstics are embedded into regression model by the 2 assumptions:
1. There exists a probability distribution of Y for each level of X
2. The means of these probability distributions vary in some systematic fashion with X.

Essentially what we get is Y is a random variable with parameter X.

So for ex when X is a value like 4, Y has a distribution which takes 4 as a parameter and certain probability distribution of Y and the actual value of Y is a 
random selection from this probability distribution.

The means of these probability distributions have a systematic relationship with the independent variable x.
This systematic relationship is called the *regression function Y on X*.
The graph of this regression function is the *regression curve*.

While the probability distribution and relationship (linear, exponential) might change, the concept of P(Y|X) is the formal explanation to the scatter in the statistical relationship.

It means that because Y is not a value but a Random Variable on x the statistical relationship is not a functional relationship.

###Construction of Regression Models

**Selection of Variables**
The variables that must be a part of the independent variables would be:
1. Variables that must reduce maximum of residual variation in Y after all the other predictor variables are added to the model.
2. Is the variable causal - does it impact the dependent variable?
3. How quickly, accurately or economically can the variable be procured?
4. Can it be controlled?

**Functional Form of Regression Relationship**
Functional form of a regression relationship is dependent on relationship of independent variables with the dependent variable. Also, experience or theory 
generally provides some guidance on how the relationship would look like. The theory would suggest what the relationship and the asymptotic properties should be for a relationship.

Intial assumptions of linear or quadratic would be a good starting point for most regression relations.


**Scope of the Model**
The scope of the model is the range of values where the model is valid. This is typically flowing in either from the data available or from the design of the experiment.

### Uses of Regression

The 3 main purposes of regression analysis are:
1. Description
2. Control
3. Prediction

### Regression and Causality	

A statistical relationship between y and x does not mean that x causes y. It only implies that y is strongly correlated with x.

Regression analysis does not provide any information about causality. Further analysis is needed to identify and establish causality.

### Simple Linear Regression Model

Simple Linear Regression model implies linear in parameters and linear in predictor variables and only 1 predictor variable.
Model that is linear in parameters and in predictor variable is called a first order model.

** Features of Linear Model**
The response variable Yi which is the ith trial for estimation of the relationship between X and Y is a sum of 2 components
				β0 + β1xi + ε
Because of the error term **ε** the prediction Yi is a random variable


			 E(Yi) = E(β0 + β1xi + ε) = β0 + β1xi + 0 

This is because E(ε) = 0. Because error term is a random variable with 0 mean and σ standard deviation.

The response variable Yi falls short or exceeds β0 + β1xi by ε.

The variation in ε is assumed to be constant and is represented by σ^2

Since all the other parameters are constants variation in predictor variable Y is also σ^2.

The error terms are assumed to be uncorrelated. Since error terms are uncorrelated and other terms in the regression estimate are constants Yis are also assumed to be uncorrelated.


So, a regression model is formally defined as a function in which the dependent variable Yi comes from a probability distribution whose mean is  
				E(Yi) = E(β0 + β1xi + ε) = β0 + β1xi
and whose variance is σ**2.



** Meaning of Regression Parameters**

			 β1 --> Slope of the regression line. It provides the change in Y for unit change in X.
			 
			 β0 --> When the model includes 0 in the prediction, it provides the mean of distribution or prediction for Y when X=0. When X=0 is not a part of the model it doesnt have any interpretation.
			 
			 
### Data for Linear Regression Model

**Observational Data**
It is collected from nonexperimental studies. We cant control the dependent or independent variables in such data. 

Major limitation of observational data is that establishing causality is a challenge.
 

**Experimental Data**
The data is collected by process or approach where we can control the independent variables.	

Establishing causality in this design is easier because we control the independent variable. Hence the independent variable is called the *treatment* and the participants in the 
problem are called *experimental units*

### Esimating the Regression Function

**Method of Least Squares**

The most intuitive and simple explanation of identifying the coefficients for a simple Linear Regression is the least squares method

It tries minimizing the    ∑\(yi-β0 + β1xi\)^2 for all the N observations collected

Partial diffentiation with respect to the 2 parameters b0 and b1 gives 2 equations in 2 unknowns solving for which we get the unbiased estimates for the parameters 
β0 and β1.

**Point Estimate for Mean Response**

The value 
				Yihat = b0 + b1xi
				
This value is the point estimate for Y because it is the means response. Mean of the P(Y|X) corresponding for a particular X of interest.


**Properties of the Regression Line **

1. Sum of all the residuals ∑ei = 0

2. Sum of squared residuals is minimized

3. Sum of observed and expected values is equal i.e ∑Yi = ∑Yihat

4. The sum of weighted residuals by independent variable is 0  ∑Xiei=0

5. Following for point 4 ∑Yiei=0


### Estimating the Error Term's variance

** Point Estimate of σ^2

For a single population whose mean is unknown, the sample variance s^2 is an unbiased estimate of σ^2


				s^2 == ∑(Yi - Ybar)^2/ n-1
				
n-1 is the degrees of freedom because 1 degree is lost because of using Ybar as an estimate of population mean


To estimate σ^2 from regression model, we know that the variance in Y is the same a variance in ε which is σ^2

We also know that Yihat the estimator of Yi now comes from a distribution around Xi.
Hence the error term around Yihat the estimation of Yi is the error term ei
				Yi-Yihat = ei
				
This is the error in prediction. The SSE (sum of squared of error) will be:

				SSE = ∑(Yi - Yihat)^2


In this case the s^2 unbiased estimator for σ^2 would be:
				s^2 = MSE == SSE/n-2
				
The 2 degrees of freedom lost are the 2 parameters b0 and b1.


### Normal Regression Model
Without making any assumptions about the distribution of the error terms, the unbiased point estimates for β0 and β1
have the least variance among all the unbiased estimators.

To setup interval estimates and make test we need to make assumptions of the error terms. The standard assumption of error term is 
that it is normally distributed around 0 with variance σ^2.

This assumption simplifies the analysis singificantly and is reasonable in most real world situation.
				
The regression model is:
				
				Yi = β0 + β1xi + εi
				
where εi are independent with 	N\(0,σ^2\)


**Estimation of parameters of regression by MLE **

The error terms εi = (Yi - β0 + β1xi) are now normally distributed around 0 with variance σ^2


so for              ei = (1/sqrt(2π)σ )\* e^-((Yi - β0 + β1xi)/σ)^2


Our objective is to minimize the errors for all the samples we have collected. This can be achieved by mutiplication of all the errors and minimizing it

This would translate to 

                 L(ei) = π \[(1/sqrt(2π)σ )\* e^-((Yi - β0 + β1xi)/σ)^2\] for all N observations
						
					   = (1/(2πσ)^n/2) \*  e^ -(1/2σ^2) ∑ (Yi- β0 + β1xi)^2

Taking the log of this equation makes the math easier

						= -1/2σ^2 ∑ (Yi- β0 + β1xi)^2
						

Differentiating the above equation wrt to the parameters in the equation  β0, β1 and σ^2 and setting them to 0 gives the estimates of these parameters.


				 
