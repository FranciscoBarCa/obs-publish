#machine_learning #model_performance
 ![[../assets/Confusion matrix 2023-02-10 20.20.11.excalidraw]]
 True positives: We correctly predicted true
 True negatives: We correctly predicted false
 False positives: We incorrectly predicted true. It was actually false but we predicted true
 False negatives: We incorrectly predicted false. It was actually false but we predicted true
> [!tip] We prefer false positive to false negative. (Over detect illness)

## Accuracy
(Most Important)
Percentage of correct predictions	    $$ Accuracy = \frac{TP + TN}{TP + TN + FP + FN} $$
## Precision
Percentage of positive predictions that were correct
$$ Precision = \frac{TP}{TP + FP} $$

> [!info] Ratio of the LEFT side of the matrix


## Sensitivity (Recall)
Percentage of actual positives that were correctly predicted. Also called TPR
		       $$ Sensitivity = \frac{TP}{TP + FN} $$
		      Ratio of real positives that will be correctly identified
> [!info] Ratio of the TOP side of the matrix
## Specificity
Percentage of actual negatives that were correctly predicted. Also called TNR
		       $$ Specificity = \frac{TN}{TN + FP} $$
> [!info] Ratio of the BOTTOM side of the matrix

## FPR (False Positive Rate)
Percentage of actual negatives that were incorrectly predicted  $$ FPR = \frac{FP}{FP + TN} $$
# Code
**Make sure the output of the model has the correct format**
## Training
Y ⇾ $y$ Real
LRpred ⇾ $\hat{y}$ predicted
```{r}
confusionMatrix(
  data = fTR_eval$LRpred, # Predicted classes
  reference = fTR_eval$Y, # Real observations
  positive = "YES"
) # Class labeled as Positive
```
## Test

```{r}
confusionMatrix(
  data = fTS_eval$LRpred, # Predicted classes
  reference = fTS_eval$Y, # Real observations
  positive = "YES"
) # Class labeled as Positive
```