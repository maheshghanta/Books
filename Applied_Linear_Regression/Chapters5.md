## Chapter 5 Matrix approach to Simple Linear Regression

### Matrices

**Definition of Matrix**

A rectangular array of elements arranges in rows and columns.

A matrix typically is represented as  **A** - a bold character. The dimensions are represented as mxn where m is the number of rows and n is the number of columns.

**Square Matrix** Matrix of mxn dimensions where m = n 
**Vector** Matrix containing only 1 column is a column vector, 1 row is called a row vector
**Transpose** Transpose interchanges the rows to columns. Hence a mxn matrix become nxm.
**Equality of Matrices** 2 matrices are called equal only when each element of the matrix equals the element of the other matrix in the same location.

### Special Type of Matrices 

**Symmetric Matrix** If Transpose(A) = A then the matrix is symmetric
**Diagonal Matrix** If all the elements other than the diagonal elements are 0 then the matrix is a diagonal matrix
**Identity Matrix** Matrix with diagonal elements 1 and all the others 0 is an identity matrix.

### Linear Dependence and Rank of a Matrix

**Linear Dependence**

If any column of a matrix is a linear function of any other column in the matrix it is linear dependence of columns of the matrix.

If  c scalars not all 0 can be found such that:
				k1C1 + k2C2 + ... kcCc
Then the columns are linearly dependent. If all the values of k are 0 then the columns are linearly independent.

**Rank of a Matrix**
The rank of a matrix is defined as number of linearly independent columns or rows of a matrix.


### Inverse of a Matrix

Inverse of a matrix is such a matrix that multiplied by the matrix results in an Identity matrix.
				
				Inverse(A) A = A Inverse(A) = I
				


**Finding the Inverse**

Inverse of a square matrix rxr will exist only if the matrix has a rank of r.  i.e. all the columns / rows must be linearly independent.


**Uses of Inverse**

Similar to algebra where inverse helps finding the value of a variable. Inverse of a matrix helps finding the values of vector of variables easily.

					AY = C
					Inverse(A) A Y = Inverse(A)C
					Y = Inverse(A)C
					

### Random Vectors and Matrices

**Expectation of Random Vector or Matrix**

Suppose that a vector contains 3 observations in the matrix Y 

				Y = [Y1 Y2 Y3]
				
				E(Y) = [E(Y1) E(Y2) E(Y3)]
				
				Hence the expected value of a vector of random variables is a vector whose elements are expected values of each of random variables in the vector.
				
				Same applies to a matrix, where Expected value of each element which is a random variable in itself.
				
				

**Variance Covariance Matrix of a Random Vector**


					[ σ2Y1 		σ(Y1,Y2)	σ(Y1,Y3) ]
			σ2(Y) = [ σ(Y1,Y2)  σ2Y2		σ(Y2,Y3) ]
					[ σ(Y1,Y3)  σ(Y2,Y3)	σ2Y3     ]
					
					


### Multivariate Normal Distribution

Density function can be represented as a matrix form.

			
			
			Y the observation matrix is a px1 matrix for each of the Y different observations
			
			E{Y} the μ matrix will also be a px1 matrix with constants μ which are expected values of each of the random variables in Y
			
			∑  is a pxp matrix similar to the one in variance covariance matrix above.
			
			
			The density function f(Y) is given as below:
			
			f(Y) = (1/ (2π)^(p/2) * |∑|^(1/2)) * exp(-1/2 *  transpose(Y-μ) Inverse(∑) (Y-μ))
			
			
### Simple Linear Regression in matrix form

			Y = Xβ + ε
			
			where 
			
			Y is a nx1 vector with n observations
			
			X is a nx2 matrix with 1 vector containing only 1s for the β0 estimate and nx1 matrix of x values.
			
			β is a 2x1 matrix of  of parameters β0 and β1 [β0 β1]
			
			ε is a nx1 vector of error terms.
			

### Least squares estimation of Regression Parameters


			n b0+ bl ∑Xi = ∑Yi
			
			b0 ∑Xi + b1 ∑xi^2 = ∑XiYi


			Converting it into matrix form
			
			[n 	   ∑xi][b0]   = [∑Yi  ]
 			[∑xi ∑xi^2][b1]   = [∑XiYi]
				

			The value above is nothing but  Transpose(X)X where X is a nx2 matrix of 1s and value of X
			
			
			Hence the above equation becomes
			
			Transpose(X)X b = Transpose(X) Y
			
			Applying the Inverse 
			
						 b  = Inverse(Transpose(X)X) Transpose(X) Y
						