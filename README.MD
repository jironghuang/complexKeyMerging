## Merging based on complex keys

I did a simple search online on merging datasets using R but was surprised that such a simple function doesn't exist.

Hence, I took the liberty to develop a simple function (complex_key_merging) in this package complexKeyMerging here. 

In future, I may embed this as part of a wider utility package. But meanwhile, you may install this package with the following steps,

- library(devtools)
- install_github("jironghuang/complex_key_merging")

## How to use it

### Full Join
complex_key_merging(dataset1, dataset1, c("variable1", "variable2"), c("variable1", "variable2"), all = TRUE)    

### Left Join
complex_key_merging(dataset1, dataset1, c("variable1", "variable2"), c("variable1", "variable2"), all.x = TRUE)

### Right Join
complex_key_merging(dataset1, dataset1, c("variable1", "variable2"), c("variable1", "variable2"), all.y = TRUE)

Update:
- Seems like this function is captured by left_join, right_join, etc under dplyr or tidyr but oh well..

