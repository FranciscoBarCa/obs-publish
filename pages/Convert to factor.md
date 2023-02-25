#machine_learning #datasets #r_language 
## Overwrite variable
Variable Y of Fdata
```r
factorCols <- c("Y")

fdata <- fdata %>%
  mutate(across(
    .cols = all_of(factorCols),
    .fns = factor
  ))
```
## New variable

```r
fdata <- fdata %>%
mutate(Y_factor = as.factor(Y))
```
