---
aliases: R^2 R2, R2 coefficient, coefficient of determination,R-squared
---
# R^2
> [!info] Note: #card
> ⏫R^2 ⇾⏫% of [Variance](Variance.md) explained ⇾ ✅Fit

What percentage of what happens can be explained by the model.
$$ 
\bar{R^2}=\frac{ESS}{TSS}=1 - \frac{RSS}{TSS} 
$$
[[ESS]] Explained error
[[RSS]] Error in prediction the prediction of y
[[TSS]] Total variance in y


Therefore, The $R^2$ measures the p**ercentage of variance that is predicted my the model**

$$
\bar{R^2}=\sum_{i=1}^{N}(\hat{y}[i]-\overline{{{y}}})^{2}+\sum_{i=1}^{N}(y[i]-\widehat{y}[i])^{2}
$$
$$
\bar{R^2}= 1 - \frac{RSS}{RS}
$$

> [!warning] Importante #card
> If we add more features to the model (even if they are not relevant) the R^2 is artificially increase -> [Adjusted R 2](#Adjusted%20R%202)


# Adjusted R^2
$$
 overline\overline{R}^{2}=1-{\frac{R S S/(N-n-1)}{T S S/(N-1)}}=1-(1-R^{2}){\frac{N-1}{N-n-1}}
$$
