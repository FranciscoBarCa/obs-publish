---
alias: Colinearity
---

#machine_learning #datasets
> [!warning] Importante #card
> if there are two very correlated inputs it can mess up the model. 


If two predictors are highly correlated, they are **measuring the same underlying information**
When two predictors are very **strongly correlated**, including both in a model may lead to confusion or problem with a **singular matrix**.

We measure with [Variance Inflation Factor (VIF)](Variance%20Inflation%20Factor%20(VIF).md)
# Problems
- Unstable models -> Matrix 
- Degraded predicted performance
- Misleading explanations
# Solutions:
 - **Remove one of the variables** with high correlation
 - Combine the variables into a single variable (e.g., average) -> THe one with the 
-  Use a dimensionality reduction technique (eg.,[[PCA]])

# Measure 
 [Variance Inflation Factor (VIF)](Variance%20Inflation%20Factor%20(VIF).md)
## Heuristic algorithm
Section 3.5 of “Applied Predictive Modeling” ([Kuhn and Johnston 2013](https://scientistcafe.com/ids/collinearity.html#ref-APM)) presents a heuristic algorithm to remove a minimum number of predictors to ensure all pairwise correlations are below a certain threshold

> 1.  Calculate the correlation matrix of the predictors.
> 2.  Determine the two predictors associated with the largest absolute pairwise correlation (call them predictors A and B).
> 3.  Determine the average correlation between A and the other variables. Do the same for predictor B.
> 4.  If A has a larger average correlation, remove it; otherwise, remove predictor B.
> 5.  Repeat Step 2-4 until no absolute correlations are above the threshold.

The **`findCorrelation()`** function in package `caret` will apply the above algorithm.

```
(highCorr <- findCorrelation(cor(sdat), cutoff = 0.7))
```

```
## [1] 2 6
```

It returns the index of columns need to be deleted. It tells us that we need to remove the 2nd and 6th columns to make sure the correlations are all below 0.7.

```
# delete highly correlated columns
sdat <- sdat[-highCorr]
# check the new correlation matrix
(cor(sdat))
```

The absolute value of the elements in the correlation matrix after removal are all below 0.7. How strong does a correlation have to get, before you should start worrying about multicollinearity? There is no easy answer to that question. You can treat the threshold as a tuning parameter and pick one that gives you best prediction accuracy.

# Plotting
There is an excellent function in `corrplot` package with the same name `corrplot()` that can visualize correlation structure of a set of predictors. The function has the option to reorder the variables in a way that reveals clusters of highly correlated ones.

```r
# select non-survey numerical variables
sdat <- subset(sim.dat, select = c("age", "income", "store_exp", 
    "online_exp", "store_trans", "online_trans"))
# use bagging imputation here
imp <- preProcess(sdat, method = "bagImpute")
sdat <- predict(imp, sdat)
# get the correlation matrix
correlation <- cor(sdat)
# plot
par(oma = c(2, 2, 2, 2))
corrplot.mixed(correlation, order = "hclust", tl.pos = "lt", 
    upper = "ellipse")
```
≈ 0 ⇾ ⏫ lighter color and  ⏬ elliptical
![](../assets/Pasted%20image%2020230220141925.png)


![[../assets/Correlation 2023-02-15 16.08.49.excalidraw]]
