---
aliases: cross-validation, cross-Validation Cross-validation
---
> [!info] Note: #card
>Cross-validation helps to reduce variability and, therefore, limit [[overfitting]].


In a **conventional validation setting**, the original data is partitioned into three subsets, usually  60% for the [[training set]], 20% for the [[Validation set]], and the rest (20%) for the [testing set](test%20set.md).

**But** if this only works if we have **enough training samples after partitioning**, and we only need a **rough estimate** of simulated performance. **Otherwise, cross-validation is preferable.**

> [!info] Note: #card
> Bascilally we use all data to test and validate by partitioning many imes and averaging the results.


> [!warning] Importante #card
> ⏫ Data ⇾ Training, Validation Testing
> 
>⏬ Data ⇾ Cross-validation (otherwise it would be computationally expensive.)

There are two types:
# K-fold cross-validation
> [!info] Note: #card
> Lower variance compared to LOOCV (we're using a chunk of samples instead a single one for validation).

We divide the data in K folds. We train the model with K-1 folds and a [[test set]] with the remaining fold. We repeat this process K times.
![|200](../assets/Pasted%20image%2020230212154636.png)
Thereafter, we average the results.

        $$ CV = \frac{1}{K} \sum_{i=1}^{K} MSE_i $$

> [!note] We usually use 10 folds

# LOOCV
> [!info] Note: #card
> Only suitable for small datasets

We exclude just **one sample** of the [[train set]].
For a dataset of the size n, LOOCV requires n rounds of cross-validation. 
This can be slow when n gets large.
![|300](../assets/Pasted%20image%2020230212154524.png)
# Performance estimating MSE
The [Expected Test Error](Expected%20Test%20Error.md) is shown in blue🟦.
Using [LOOCV](#LOOCV) is black ⬛.
Using [K-fold cross-validation](#K-fold%20cross-validation) in orange 🟧.
> [!info] Note: #card
> [[MSE]] is always **underestimated**. And we can get a good estimation with [K-fold cross-validation](#K-fold%20cross-validation) with much less work than [LOOCV](#LOOCV)

![](../assets/Pasted%20image%2020230212154832.png)




## RSS
Sum of Squared Errors (or Residual Sum of Squares):
$R S S=\sum_{i=1}^{N}(y[i]-{\hat{y}}[i])^{2}$