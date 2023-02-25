#machine_learning #r_language 
## Boxplot

A **boxplot** is a graph that shows the distribution of a variable. It is made up of a box and two whiskers. The box shows the **interquartile range** (IQR) of the data. The whiskers show the range of the data. The median is shown as a line inside the box. Outliers are shown as points outside the whiskers.

```r
fdata %>%
  select(where(is_bare_numeric)) %>% # Only pure numeric
  pivot_longer(cols = everything(), names_to = "variable") %>%
  ggplot(aes(x = value)) +
  geom_boxplot() +
  ylim(-0.6, 0.6) + # manual proportion adjustment
  facet_wrap(~variable, scales = "free", ncol = 2)
```
![](../assets/Pasted%20image%2020230209220934.png)