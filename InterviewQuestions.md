## Q : Does a lower mean square error MSE of model imply better fit for data?

Not necessarily.
MSE for multiple linear regression MLR will be smaller than MSE for simple linear regression SLR. Since the errors of the data will decrease when variables are added.
___

## Q : What is a good R-Square value for a model?

Model with higher R-sq value is better fit for data.Its value ranges from -1 to 1 . So more the value is closer to 1 more accurate our model is .
___

## Q : What is a good Mean Sqaure Error MSE Value for a model?

Model with smallest mean square error MSE value is good fit for data. Adding more variables can reduce MSE value.
___

## Q : What happens to Mean Square Error MSE
   ###    1. Train data
   ###    2. Test data
## when the order of the polynomial increases ?

On Train Data:
As the order of the polynomial increases the MSE of train data decreases.
<img src="images\Overfitting-Underfitting-and-Model-Selection-Coursera.png">

On Test Data:
As the order of the polynomail increases the MSE increases.It is because of the noise often called as irreduceable error. **y(x) + noise**
<img src="images\test error.png">


___

## Q : What is Ridge Regression ?

Ridge regression is a regression that is employed in a Multiple regression model when Multicollinearity occurs. Multicollinearity is when there is a strong relationship among the independent variables. Ridge regression is very common with polynomial regression
**Ridge Regression prevents overfitting.**
Here we introduce a parameter called *alpha*. The higher the value of *alpha* the coefficients value decrease closer to 0. There is some important range of *alpha* values as follow:
0
0.001
0.01
1
10
The most used value is *alpha* = 0.01 . Again this can vary from model to model.
**Higher *alpha* values can underfit our data and lower *alpha* values can overfitt the data.**
To choose best *alpha* value for our model note the value of R-square on test data
while changing *alpha* values on every cycle.
Then pick the *alpha* value which generates highest R-square value for our model. 
Sometimes the problem of overfitting worsens when we have lot of features and what happens is that Rsquare value decreases on train data with same *alpha* value but increases on validation set.But checking the same *alpha* value on test set can perform well.
