#machine_learning #classification 

It has a built in **feature selection** so we can feed many variables and it will chose the most relevant separators to do the trimming

## Algorithm
> [!info] It can only do one variable at a decission. So the boundries are square / pixelated 

Divide input space with decisions
- Categorical: Is X?
- Continuous X > i?
![](../assets/Pasted%20image%2020230201150707.png)
### Continuous algorithm
We project data into an axis and try all possible predictors values between points. We chose the predictor leads to the highest purity(**lowest gini**) after the split.
![](../assets/Pasted%20image%2020230201152314.png)
To calculate the probability we count samples in each region.
![](../assets/Pasted%20image%2020230201152524.png)
![](../assets/Pasted%20image%2020230201152538.png)
### Categorical algorithm
We divide categorical variables as binary variables. and   and again try to make pure
## Purity
The less separators (nodes) we use to create the space the more pure it is (ej 
green)
We have mutiple measures of impurity.
### Gini index
$$Gini = 1-\sum_{i=1}^m p_{1}^2$$

> [!abstract] How homogeneous is the node

> [!important] The sooner the decission was taken, the larger the relevance of the variable.


### Entropy
![](../assets/Pasted%20image%2020230201152707.png)
## Stopping cirteria / Pruning
To reduce the complexity we add a parameter to punish complexity called $C_{P}$

> [!important] The higher the Cp the more we are punishing performance. Simpler model

> [!important] High complexity-> high variance

# R code
#r_language
```r
library(tree) modelFit = tree(Y ~ X1 + X2, fdata_train) summary(modelFit) #Show information of the model 
modelFit #show model cuts in text 
plot(modelFit) #Plot the splits of the tree 
text(modelFit) #Add the labels to the tree plot 
tree.pred= predict(modelFit , fdata_val, type ="class") #predict
```
## tree pruning
```r
prune. modelFit =prune.misclass(modelFit ,best =15)
```
## Cross-Validation
```r
cv.modelFit =cv.tree(modelFit ,FUN=prune.misclass)
```
