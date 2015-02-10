# Swirl Learning

Contents:

- [Workspace](#Workspace)
- [Write .csv file from data loaded in R](#write.csv)

<a name="Workspace"/>
## Workspace
### list of variables
+ Type ls() to see a list of the variables in your workspace
  - type rm(list=ls()) to clear your workspace
 

<a name="write.csv"/>
## write.csv
### Write .csv file from data loaded in R
+ write.csv(by_package, file = "by_package.csv")



<a name="tidy"/>
## tidy
### load tidy library
+ library(tidyr)
+ tidy data satisfies three conditions:
  - 1) Each variable forms a column
  - 2) Each observation forms a row
  - 3) Each type of observational unit forms a table
+ gather()
  - res <- gather(students2,sex_class,count,-grade)
+ separate()
  - separate(data=res,col = sex_class, into = c("sex", "class"))
