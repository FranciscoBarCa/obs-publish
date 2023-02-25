#machine_learning #regression 
# How it works
## Formulation
Basic line consisting of weights of variables in estimation and bias(wo)
$$
y=w_{0}+w_{1}x_{1}+w_{2}x_{2}+\ldots+w_{n}x_{n}=w^{T}x
$$

The weight vector $w$ is learned from the [training data](training%20data.md), with the goal of **minimizing the estimation error** defined as mean squared error ([Mean Square Error](Expected%20Test%20Error.md))

## Cost function
We try to minimize J(w) using [Gradient Descent](Gradient%20Descent.md)
$$
J(w)=\frac{1}{m}\sum_{i=1}^{m}\frac{1}{2}\left(\hat{y}(x^{(i)})-y^{(i)}\right)^{2}
$$
The derivative for gradient descent is: 
$$
\Delta w=\frac{1}{m}\sum_{i=1}^{m}\left(-\,y^{(i)}+\hat{y}(x^{(i)})\right)x^{(i)}
$$
Which is updated according to the [[learning rate]] $\eta$ 

# Why to use it

# Code 


