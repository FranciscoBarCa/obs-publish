k#machine_learning  #model_performance 
>[!tip] Kappa measures the performance of a model relative to a random model.

> [!info] 
>  It is a good measure of accuracy when the classes are imbalanced.

It measures the **agreement** between the **observed** and **predicted** classes.  
$$ Kappa =\kappa = \frac{P_O - P_e}{1 - P_e} $$
 $P_{O}$ ⇾ Observed [Accuracy](Confusion%20matrix.md#Accuracy) (seen on model)
 $P_{e}$ ⇾ Expected: [Accuracy](Confusion%20matrix.md#Accuracy) if randomly assigned the category.  (this is what considers class imbalances)   $$P_{e}=\frac{(TP+FP)(TP+FN)+(FN+TN)(FP+TN)}{n^{2}}$$
 | Kappa      | Agreement                  |
 | ---------- | -------------------------- |
 |  > 0       | Worst than chance agreement(random)                         |
 | < 0        | Less than chance agreement |
 | 0.01–0.20  | Slight agreement           |
 | 0.21– 0.40 | Fair agreement             |
 | 0.41–0.60  | Moderate agreement         |
 | 0.61–0.80  | Substantial agreement      |
 | 0.81–0.99  | Almost perfect agreement   |

> [!warning] Importante #card
>  0.3 to 0.5 indicates a reasonable agreement.

