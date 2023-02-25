---
aliases: probabilistic classification, soft classification
---
alias: 
#machine_learning #classification 

The output variable is **continuous**. 
We express the probability of it being true.
We can use a threshold to get a binary output variable.

$${\hat{p}}(x)={\hat{P}}\left({\frac{y=1}{x}}\right)$$
Probability of Y being true given the input parameters (x)
We are using the [Bayes Theorem](Bayes%20Theorem.md)
![|400](../assets/Pasted%20image%2020230210175600.png)
$${\hat  {y}}=\operatorname {\arg \max }_{{y}}\Pr(Y=y\vert X)$$
> [!warning] Importante #card
> The predicted class is that which has the highest ⏫ probability.





## Example:
Weather forecast. The output variable is the probability of rain. We can use a threshold to get a binary output variable.

  
