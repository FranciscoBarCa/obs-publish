#machine_learning  #r_language 
```run-r
fdata %>%
  select(where(is_bare_numeric)) %>% # Only pure numeric
  pivot_longer(cols = everything(), names_to = "variable") %>%
  ggplot(aes(x = value)) +
  geom_density() +
  facet_wrap(~variable, scales = "free", ncol = 2)
```
![](../assets/Pasted%20image%2020230209221232.png)
