---
aliases: MSE, Mean Square Error 
---
> [!info] Note: #card
> We can estimate the it by using [Cross Validation](Cross%20Validation.md)

$$ E (y_o -\hat{y})^2 = Var(\hat{y}) + (Bias(\hat{y}))^2 + Var(\epsilon) $$ 	$$ E (y_o -\hat{y})^2 = Variance + Bias^2 + Noise $$The first term refers to the average test MSE that we would obtain if we repeatedly estimated f using many training sets and tested  each at x0
![|300](../assets/Pasted%20image%2020230212105324.png)
1. ⏬ [Variance](Variance.md) ⏫ [Bias](Bias.md)
2. ⏫ [Variance](Variance.md) ⏫ [[Bias]]
3. ⏬ [Variance](Variance.md) ⏬ [Bias](Bias.md) 
4. ⏫ [Variance](Variance.md) ⏬ [Bias](Bias.md)
