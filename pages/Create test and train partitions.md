#machine_learning #datasets #r_language 

```r
set.seed(2023)
outCol <- grep(outVar, names(fdata))

trainIndex <- createDataPartition(fdata[, outCol] %>% pull(), # output variable.
  p = 0.8, # split probability for training
  list = FALSE, # Avoid output as a list
  times = 1
) # only one partition

fTR <- fdata %>%
  slice(trainIndex)

fTS <- fdata %>%
  slice(-trainIndex)
```

