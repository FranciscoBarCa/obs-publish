
#classification #machine_learning 
> [!info] We can change the 

![](../assets/Pasted%20image%2020230201162022.png)
## Bagging
For continuous variables we average the results of multiple [Decision Trees](Decision%20Trees.md) to reduce the variance of the parameters.
$$\hat{f_{bag}(x)}= \frac{1}{B}\sum \hat{f(x)}$$
For categorical variables we use the majority.
### Bootstrapping
![](../assets/Pasted%20image%2020230201154224.png)
We pick the data at random, and allow to repeat data when creating new datasets.
## Algorithm
![](../assets/Pasted%20image%2020230201155014.png)

> [!warning] The interpretation of a random forest is much harder than a decision tree as we are using multiple decision trees in paralell.
> 

# R code
#r_language 
```r
# Required libraries for random forest models
library(randomForest)

set.seed(150) #For replication

# Train Random Forest Model

# rf contains one tuning parameter mtry: 
# that is the number of variables randomly sampled as candidates at each split.
# The ntree argument can be used to specify the number of trees to grow.

rf.fit <- train(Y ~ .,   # Model formula
                data = fTR,
                method = "rf", # Random forest
                ntree = 200,  # Number of trees to grow
                tuneGrid = data.frame(mtry = seq(1, ncol(fTR) - 1)),           
                # tuneLength = 4,
                trControl = ctrl, # Resampling settings 
                metric = "Accuracy") # Summary metrics


rf.fit # Information about the resampling settings

ggplot(rf.fit) # Plot the summary metric as a function of the tuning parameter

summary(rf.fit)  # Information about the model trained

rf.fit$finalModel # Cuts performed and nodes. Also shows the number and 
# percentage of cases in each node.

# Measure for variable importance
varImp(rf.fit,scale = FALSE)
plot(varImp(rf.fit,scale = FALSE))

```
