# Learning from Swirl (and other sources)

Contents:

- [Help](#Help)
- [Workspace](#Workspace)
- [Write .csv file from data loaded in R](#write.csv)

# A


# H
<a name="Help"/>
## Accessing the help files for built in functions
### accesing help on a specific topic
+ access help on spread() by typing ?spread
+ access help on library() by typing ?library


# W
<a name="Workspace"/>
## Workspace
### list of variables
+ Type ls() to see a list of the variables in your workspace
  - type rm(list=ls()) to clear your workspace

<a name="write.csv"/>
## write.csv
### Write .csv file from data loaded in R
+ write.csv(by_package, file = "by_package.csv")


# T
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


# S
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

## Structure
+ display the dtructure of an arbitrary R object
+ provides useful summary on dataset
  - str(x)

## View
+ displays the dataset in tabular form
+ note the capital V
  - View(x)

## summary
+ summary of data
  - summary(x)
+ summary of subset of data (summary of column)
  - summary(x$age)

## matrix
+ create matrix of elements
  - matrix(data = NA, nrow = 1, ncol = 1, byrow = FALSE,dimnames = NULL)
+ matrix with four elements 1,2,3,4 in 2 rows
  - matrix(1:4,2)

## table
+ tabular summary of subset of data
  - summary(x$age)
+ prop.table returns table entries as fraction of the marginal table
  -  m <- matrix(1:4,2)
  -  m
  -  prop.table(m,1)

## %>%
+ chaining commands - read as "then"
  - student_info <- students4 %>%
  
    select(id, name, sex) %>%
  
  - this stores the result of the select in student_info

## select
+ select(x,age) returns only column age

## unique
+ eliminates duplicate rows

## mutate {dplyr}
+ add new column called status to table called passed
+ assign the value "passed" to each row in table
+ store the table with extra column in same table called passed
  -  passed <- passed %>% mutate(status = "passed") 

