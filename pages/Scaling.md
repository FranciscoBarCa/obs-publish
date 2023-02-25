Scaling can severely affect the **perceived distance between points**. This is a issue for many algorithms, especially those that use distance metrics. For example, the k-nearest neighbors algorithm will give different results depending on the scale of the data.
   
Many Machine Learning algorithms are affected by the scale of the predictors (e.g., distance functions).

![](../assets/Pasted%20image%2020230209224024.png)

To solve it, we apply [[Standarization]].

To measure of

## Z-score

The **Z-score** is the number of standard deviations from the mean a data point is. The formula is:

$$ Z = \frac{X - \mu}{\sigma} $$

Where $X$ is the value of the data point, $\mu$ is the mean of the data, and $\sigma$ is the standard deviation of the data.

The Z-score is a measure of how many standard deviations away from the mean a data point is. A Z-score of 0 means that the data point is exactly at the mean. A Z-score of 1 means that the data point is 1 standard deviation above the mean. A Z-score of -1 means that the data point is 1 standard deviation below the mean.