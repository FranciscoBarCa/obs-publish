#machine_learning 
# Basic Libraries
```r
library(tidyverse)
library(caret)
library(MLTools)
library(pROC) # for plotting ROC curves.
library(skimr) # for dataset initial exploration
```
# Set working directory
We are using a WSL Vm so we need to use this path notation
```r
print(getwd())
wd <- "/mnt/c/Github/Lab-Machine-Learning/P1" # WSL
#wd <- "C:/Github/Lab-Machine-Learning/P1"
setwd(wd)
```
# Load dataset

Import from csv
```r
library(tidyverse)
filename <- "MortgageClass.csv"
fdata <- read_csv(filename)
fdata %>% head()
```
import from tsv
```r
fdata <- read_tsv("SimData.dat", )
```

# Clean dataset

## Remove duplicate
```r
fdata <- fdata %>% 
  filter(!duplicated(.))
```
## Remove missing values
### Check amount of missing
```r
fdata %>% 
  complete.cases %>% 
  all
```
### Drop missing
if the percentage is small
```r
fdata <- fdata  %>% 
  drop_na()
```