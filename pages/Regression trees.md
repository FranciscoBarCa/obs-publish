#machine_learning #regression 
[Decision Trees](Decision%20Trees.md) with a continuous output
Also its brother -> [[Regression forest]]
# How it works
A regression tree is constructed by **recursive binary splitting and growing** each node into left and right children. In each partition, it greedily searches for the **most significant** combination of **feature and its value** as the **optimal splitting point**. 
![](../assets/Pasted%20image%2020230222154617.png)
## Quality of separation
The **quality** of separation is measured by the weighted purity of labels of two resulting children, specifically via metric [MSE](MSE.md)
## Estimated value
The value is computed as the **average** of the value of y of the samples inside that leaf. Eg:
![](../assets/Pasted%20image%2020230215144617.png)
> [!info] Note: #card
>  We can also combine this with [Regression splines](Polynomial%20Regression.md#Regression%20splines) to further improve the model.
# Why use it

## Advantages
• They are **highly interpretable** and are easy to implement  
• They can effectively handle many types of predictors (**sparse, skewed,  
continuous, categorical, etc.**) **without the need to pre-process** them  
• They can effectively handle missing data and implicitly conduct [Feature Selection](Feature%20Selection.md)
## Problems:
• **Model instability** (i.e., slight changes in the data can drastically change the structure of the tree or rules and, hence, the interpretation) -> [Regression forest](Regression%20forest.md)  
• Less-than-optimal predictive performance. If the relationship between  
predictors and the response cannot be adequately defined by rectangular  
subspaces of the predictors, then tree-based or rule-based models will  
have larger prediction error than other kinds of models.

# Code
