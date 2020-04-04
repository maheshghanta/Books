# Applied Linear Regression

Linear Regression is one of the most important and fundamental statistical techniques anyone who wants to do data analysis must be good at.
This book is one of the comprehensive books that discusses about this technique.
The	book can be bought from here [Amazon](https://www.amazon.in/Applied-Linear-Regression-Probability-Statistics/dp/1118386086/ref=dp_ob_title_bk)


## Chapter 1 Linear Regression with One Predictor Variable

1.1. Refer to the sales volume example on page 3. Suppose that the number of units sold is measured
accurately, bur clerical errors are frequently made in determining the dollar sales. Would the
relation between the number of units sold and dollar sales still be a functional one? Discuss.

Ans: No. Because for a functional relationship to exist, for any value of x the value of y= f(x) must be the same. i.e. if y = 2x.
The value for y is always fixed by the value of x. However, in this case because of some clerical errors this function would not hold and hence 
it is a statistical relationship and not a functional one.


1.2. The members of a health spa pay annual membership dues of $300 plus a charge of $2 for each
visit to the spa. Let Y denote the dollar cost for the year for a member and X the number of
visits by the member during the year. Express the relation between X and Y mathematically.
Is it a functional relation or a statistical relation?

Ans: y = 300 + 2x. Its a functional relationship because there is not uncertainity in the amount you pay for the spa.


1.3. Experience with a certain type of plastic indicates that a relation exists between the hardness
(measured in Brinell units) of items molded from the plastic (Y) and the elapsed time since termination
of the molding process (X). It is proposed to study this relation by means of regression
analysis. A participant in the discussion objects, pointing out that the hardening of the plastic
"is the result of a natural chemical process that doesn't leave anything to chance, so the relation
must be mathematical and regression analysis is not appropriate." Evaluate this objection. 

Ans: Eventhough, the process is a natural chemical process. There would be differences in the hardness of plastic. If there was no variance in the hardness
for the same process always then the question of evaluation would not have arisen. Hence, there would be a statistical relationship with some variance. 
Therefore, the objection can be overlooked.

1.4. In Table 1.1, the lot size X is the same in production runs 1 and 24 but the work hours Y differ.
What feature of regression model (1.1) is illustrated by this?

Ans:  Y is a Random Variable with error epsilon.


1.5. When asked to state the simple linear regression model, a student wrote it as follows: E {Yi} = β0 + β1Xi + εi Do you agree?

Ans: No. Yi = β0 + β1Xi + εi . Yi is a random variable. E(Yi) = β0 + β1Xi because the mean of εi is 0.


1.6. Consider the normal error regression model (1.24). Suppose that the parameter values are
β0 = 200, β1 = 5.0, and σ = 4.
a Plot this normal error regression model in the fashion of Figure 1.6. Show the distributions
of Y for X = 10, 20, and 40.

b. Explain the meaning of the parameters β0 and β1. Assume that the scope of the model
includes X = 0.

Ans: β0 is the value of y when x=0 and β1 is the increase in y for unit increase in x.


1.7. In a simulation exercise, regression model (1.1) applies with β0 = 100, β1 = 20, and  σ2 = 25.

An observation on Y will be made for X = 5.

a. Can you state the exact probability that Y will fall between 195 and 205? Explain.

Ans: No. Using equation 1.1 we didnot make any assumptions about the distribution of error. Hence, we can only arrive at a point estimate for Y but can conclusively say
what is the probability that Y falls in a interval.


b. If the normal error regression model (1.24) is applicable, can you now state the exact prob- Ii.
ability that Y will fall between 195 and 205? If so, state it.

Ans:  Here we make the assumption that the error is normal. Hence, 

 Yi = β0 + β1Xi + εi
	= 100 + 100 + εi
	=200 + εi
	
E( 195<Yi < 205) = E( -5<εi <5) = E( -1 < Z < 1)   where Z= (x-mu)/σ 
	= 0.3413 \* 2 = 0.6826


1.8. In Figure 1.6, suppose another Y observation is obtained at X = 45. Would E{Y} for this new
observation still be 104? Would the Y value for this new case again be 108?

Ans: Yes. E(Y) will still be 104. The new value can be 108 but not necessarily 108 only.


1.9. A student in accounting enthusiastically declared: "Regression is a very powerful tool. We can
isolate fixed and variable costs by fitting a linear regression model, even when we have no data
for small lots." Discuss.

Ans: Regression provides as estimate for as a fixed and a variable part. However, unless we have the behavior at X=0 we cant make any inference on the 
value of the fixed part. Hence, unless we have information of small lots or when lot =0 we cant use regression to separate fixed and variable components of a expense.


1.10. An analyst in a large corporation studied the relation between current annual salary (Y) and
age (X) for the 46 computer programmers presently employed in the company. The analyst
concluded that the relation is curvilinear, reaching a maximum at 47 years. Does this imply
that the salary for a programmer increases until age 47 and then decreases? Explain.

Ans: No. The distribution of the age of the computer programmers has not been given. It could be for 2 reasons:
1. The sample for higher ages is lower.
2. Programmers above 47 might have shifted into a different role.

Hence, it is not that the salary decreases after 47. It only implies that the salaries are not linear but curvilinear.


1.11. The regression function relating production output by an employee after taking a training
program (Y) to the production output before the training program (X) is E{Y} = 20 + .95 X,
where X ranges from 40 to 100. An observer concludes that the training program does not raise
production output on the average because β1, is not greater than 1.0. Comment.

Ans: Becase X ranges from 40 to 100. β0 is not required. In this case we must use a regression only on β1 and error term to make any conclusion.


1.12. In a study of the relationship for senior citizens between physical activity and frequency of
colds, participants were asked to monitor their weekly time spent in exercise over a five-year
period and the frequency of colds. The study demonstrated that a negative statistical relation
exists between time spent in exercise and frequency of colds. The investigator concluded that
increasing the time spent in exercise is an effuctive strategy for reducing the frequency of colds
for senior citizens.

a Were the data obtained in the study observational or experimental data?

Ans:  Observational Data. Because the the physical activity was not controlled during the data collection.


b. Comment on the validity of the conclusions reached by the investigator.

Ans: The conclusion is based on correlation and not causality. It could be the case that healthy individuals worked out more and hence they have 
more physical activity. 

c. Identify two or three other explanatory variables that might affect both the time spent in
exercise and the frequency of colds for senior citizens simultaneously.

Ans: Weather, gender, existing medical conditions etc.

