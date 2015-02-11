# Learning from Swirl (and other sources)

Contents:

- [Help](#Help)
- [Workspace](#Workspace)
- [Write .csv file from data loaded in R](#write.csv)


<a name="Help"/>
## Accessing the help files for built in functions
### accesing help on a specific topic
+ access help on spread() by typing ?spread
+ access help on library() by typing ?library

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
+ spread()
+ mutate()

## sum
+ sum(ss06hid$VAL >= 24)

## NA
+ Remove NA's from calculation
  - sum(ss06hid$VAL >= 24,na.rm = TRUE)

## download.file
+ download.file(fileUrl, destfile="./data/microdata.csv", method="curl")
  - fileurl <- "https://... "

## File and Directory Management
+ create new directory
  - dir.create("data")