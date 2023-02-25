The variance is an error from sensitivity to small fluctuations in the training set. 

Variance is the amount by which $\hat{y}$ would change if we estimated it using a different training set. It is a measure of the model's sensitivity to changes in the training data.

> [!danger] Very important #card
>High variance may result from an algorithm modeling the random noise in the training data ([[Overfitting]])


> [!important] A very robust model has ⏬ variance.
> ⏫Varaince -> [Overfitting](Overfitting.md)
# Population Variance
$$
\sigma^{2}={\frac{\displaystyle\sum_{i=1}^{N}\left(x_{i}-\mu\right)^{2}}{N}}
$$
# Sample Variance
$$
s^{2}={\frac{\displaystyle\sum_{i=1}^{n}\left(x_{i}-{\bar{x}}\right)^{2}}{n-1}}
$$
