---
aliases: error, residual
---
[[Q-Q plot]] -> Normality of residuals
[[multicollinearity]]
# Plot
```r
autoplot
```
## Good
Normal residuals 
No patters in forecast or factors -> Flat line
## Bad

Clear pattern
 U ⇾ Quadratic fit would be better for that feature
 ![](../assets/Pasted%20image%2020230215155218.png)
> Funnel ⇾ not homogeneous variance of residuals
> ![](../assets/Pasted%20image%2020230215155046.png)

Histogram not normal / Line with weight bottom -> Non-normal residuals
![](../assets/Pasted%20image%2020230215155110.png)
Vertical -> Variables is factor treated as cont
![](../assets/Pasted%20image%2020230215162705.png)

Butterfly / Bow tie -> Variables are interacting
![](../assets/Pasted%20image%2020230215163331.png)

![](../assets/Pasted%20image%2020230215163408.png)
See cif res are corr with X2
if no interaction
![](../assets/Pasted%20image%2020230215163646.png)