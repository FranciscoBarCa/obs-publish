#regression  #machine_learning 
[Linear regression](Linear%20regression.md), but with higher-order terms.
Best poly: -> [Generalized Additive Models GAMs](#Generalized%20Additive%20Models%20GAMs)

> [!danger] Very important #card
> High order terms tend to make the prediction nstable -> [[#Piecewise Polynomials]]
# Regression splines
## Piecewise Polynimials
Divide the space into areas, a fit a **lower** order model on every area.
![](../assets/Pasted%20image%2020230222150619.png)
We need to impose avoid unstable predictions.
> [!info] Note: #card
> The higher order the boundary condition, the more stable the model
 
### How it works
![[../assets/Polynomial Regression 2023-02-22 15.08.26.excalidraw]]Making data continuous
![](../assets/Pasted%20image%2020230222150759.png)
![](../assets/Pasted%20image%2020230222150926.png)
![](../assets/Pasted%20image%2020230222151013.png)

> [!info] Note: #card
> the position and number of splits is determined through [Cross Validation](Cross%20Validation.md)

To avoid overfitting at the extremes we apply: A natural spline is a regression spline with additional boundary  
constraints: the function is required to be linear at the  
boundary (in the region where X is smaller than the smallest  
knot, or larger than the largest knot)


# Smothing spline
![](../assets/Pasted%20image%2020230222153118.png)

> [!info] Note: #card
> The result is always a cubic spline


# Generalized Additive Models (GAMs)
A different model for each of the variables.
A natural way to extend the multiple linear model to allow for  
non-linear relationships is given by
![](../assets/Pasted%20image%2020230222153448.png)



## Advantages
• GAMs allow us to **fit a non-linear** 𝑓0 to each 𝑋0  so that we can automatically  model non-linear relationships that standard linear regression will miss. This  
means that we do not need to manually try out many  
transformations on each variable individually.  
• Because the model is additive, we can still examine the effect of each 𝑿 𝒋 on  Y individually while holding all the other variables fixed. Hence, if we are  interested in inference, GAMs provide a useful representation.  
• The smoothness of the function 𝑓0 for the variable 𝑋0 can be summarized via  degrees of freedom.  
## Limitations:  
• The main limitation of GAMs is that the model is restricted to be additive.  
With many variables, important **interactions can be missed**. -> we can m**anually add interaction terms**  to the GAM model by including additional predictors of the form 𝑋0 × 𝑋2 .