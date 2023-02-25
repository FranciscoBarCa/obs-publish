
> [!danger] WE need to balance the training set. But the test set should not be balanced so not to alter the model real life performance

If there is a large difference in the number of observations in each class, then the model will be biased towards the majority class. This is a problem because the model will not be able to predict the minority class well.
# Solutions
## Downsample the majority class
  This means that we randomly remove observations from the majority class until the number of observations in each class is equal.
## Upsample the minority class
  We create new data by lightly perturbing the existing data. This means that we add slightly modified copies of the existing data to the minority class until the number of observations in each class is equal.