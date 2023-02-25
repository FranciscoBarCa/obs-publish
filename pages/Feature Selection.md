#machine_learning #datasets 
Select relevant variables for predictions.

# Model dimensionality scaling
![](../assets/Pasted%20image%2020230221154820.png)
# Feature selection in [Linear regression](Linear%20regression.md)
We start with the null model (only bias no weight)
Try all models with any combination of the predictors
> [!danger] Very important #card
> We cant comapre two models with different predictors as it pusnishes complex models.

## Subset selection
### Best Subset Selection
It is just brute force
![](../assets/Pasted%20image%2020230221150850.png)
### Forward selection
[Understand Forward and Backward Stepwise Regression – QUANTIFYING HEALTH](https://quantifyinghealth.com/stepwise-selection/)
Good if: ⏫ Selectors and ⏬ data 
![](../assets/Pasted%20image%2020230221151001.png)
### Backward selection
[Understand Forward and Backward Stepwise Regression – QUANTIFYING HEALTH](https://quantifyinghealth.com/stepwise-selection/)
Good if : ⏫ Data and ⏬ selectors
![](../assets/Pasted%20image%2020230221151116.png)
### Hybrid approaches
Hybrid versions of forward and  
backward stepwise selection are available, in which  
variables are added to the model sequentially, in analogy  
to forward selection. However, after adding each new  
variable, the method may also remove any variables that  
no longer provide an improvement in the model fit.

Danger of getting into loop!



## Shrinkage methods
Try to make less complex by applying regularization.
> [!info] Note: #card
> We control complexity with lambda ()
### Ridge regression

![](../assets/Pasted%20image%2020230221151941.png)
> [!info] Note: #card
> lamda penalizes high ⏫ weights in parameters. Except intercept b0
> ⏫ Lamda -> ⏬ Parameters

> [!danger] Very important #card
> Predictors can't go to 0. They ≈ 0 so it isn't really feature selection
#### Graphical 
![](../assets/Pasted%20image%2020230221152625.png)
![](../assets/Pasted%20image%2020230221153134.png)
s -> sum of all the coefficients
### Lasso
> [!info] Note: #card
> Very similar to previous but with absolute 

![](../assets/Pasted%20image%2020230221152129.png)
![](../assets/Pasted%20image%2020230221152308.png)
> [!danger] Very important #card
> Predictors can go to 0
#### Graphical 
![](../assets/Pasted%20image%2020230221152726.png)
s -> sum of all the coefficients
![](../assets/Pasted%20image%2020230221153107.png)
## Dimension Reduction Methods
### PCA / PCR
It might be hard to detect collinearity.-> [PCA](PCA.md). We choose the predictors that maximize the variance of the model.
![](../assets/Pasted%20image%2020230221153421.png)
![](../assets/Pasted%20image%2020230221153356.png)

> [!warning] Importante #card
> Note that we are not considering the output in [[PCA]] but usually, it doesn't matter as usually, there is a good relation between the firsts principal components and the output.   (Biggest PCA explaines most of the variance)
 Solution: -> [Parcial least Squares](#Parcial%20least%20Squares)
 

### Parcial least Squares 
Similar to [[PCA]] but using the output to guide the project.
> [!info] Note: #card
> Use only if [[PCA]] works badly
![](../assets/Pasted%20image%2020230221154413.png)
## when to use which
![](../assets/Pasted%20image%2020230221154642.png)
