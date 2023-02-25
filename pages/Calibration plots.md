#machine_learning #model_performance 
assess the **agreement between predictions and observations** in different **percentiles** (mostly deciles) of the predicted values.
This of course only makes sense for [probabilistic classification](Soft%20Partitioning.md)
# Calibration
A probabilistic model is **calibrated** if I binned the test samples **based on their predicted probabilities**, each bin’s true outcomes has a proportion close to the probabilities in the bin.

# Plot
y-value -> proportion of **true outcomes**,
x-value -> the mean **predicted probability**. 
Each point represents a bin of a % of the data. Ej [0,10]
![[../assets/Calibration plots 2023-02-10 23.10.21.excalidraw]]
> [!warning] Importante #card
> the closer to the y=x line the better
> 


# Code
Its plot **1/3**
## Train
```r
PlotClassPerformance(fTR_eval$Y, # Real observations
  fTR_eval$LRprob, # predicted probabilities
  selClass = "YES"
) # Class to be analyzed
```

## Test
```r
PlotClassPerformance(fTS_eval$Y, # Real observations
  fTS_eval$LRprob, # predicted probabilities
  selClass = "YES"
) # Class to be analyzed)
```
