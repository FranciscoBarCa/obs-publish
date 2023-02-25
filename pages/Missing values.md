#machine_learning #datasets 

# Missing values

In the real world, data is often incomplete. For example, a survey respondent may choose not to share his or her income, a customer may not provide a phone number, or a sensor may fail to record a reading. In these cases, the missing data will have to be dealt with before the data can be used for analysis.
> [!info] Note: #card
> Might be a good idea to check if there is a pattern with missing values
### Amount  of data with missing values
Report the number of missing values per column of numeric data
```r
fdata %>%
  select(where(is_bare_numeric)) %>% # Only pure numeric
  pivot_longer(cols = everything(), names_to = "variable") %>%
  group_by(variable) %>%
  summarise(missing = sum(is.na(value))) %>%
  arrange(desc(missing))
```
## Large datasets
Remove the observations with missing values (small percentage)
```r
fdata <- fdata  %>% 
  drop_na()
```

## Small datasets