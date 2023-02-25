#machine_learning #r_language #datasets 
Outliers are data points in one variable that are far from the rest of the data. They can be caused by measurement errors, or they can be real observations that are very different from the rest of the data. Outliers can have a big impact on the results of a model. For example, if you are trying to predict the price of a house, an outlier can cause the model to be very inaccurate. It is important to identify and remove outliers before training a model.

# Types of outliers `%% fold %%`
## Recording errors
When one or more samples are suspected to be outliers, the  
first step is to make sure that the values are scientifically  
valid and that no data recording errors have occurred.
## Apparent outliers
With small sample sizes, apparent outliers might be a result  
of a skewed distribution where there are not yet enough data  
to see the [[skewness]].
You should use the [Distribution plot](Distribution%20plot.md) to check if it is very different from a normal distribution.
## Real outliers %% fold %%
These outliers should **not be removed.**
# Visual Methods %% fold %%
We can use some visual methods to detect outliers.
## Boxplot![Boxplot](Boxplot.md)

## Distribution plot![[Distribution plot]]

