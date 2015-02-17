# Learning from Swirl (and other sources)

Contents:

- [A](#A)  [B](#B)  [D](#D)  [F](#F)  [H](#H)  [M](#M)  [N](#N)  [S](#S)  [T](#T)  [U](#U)  [V](#V)  [W](#W)  


_________________________________________________________________________
-------------------------------------------------------------------------

## %>%
+ chaining commands - read as "then"
  - student_info <- students4 %>%
  
    select(id, name, sex) %>%
  
  - this stores the result of the select in student_info

# A <a name="A"/>


# D <a name="D"/>
## download.file
+ download.file(fileUrl, destfile="./data/microdata.csv", method="curl")
  - fileurl <- "https://... "


# F <a name="F"/>
## File and Directory Management
+ create new directory
  - dir.create("data")


# H <a name="H"/>
<a name="Help"/>
### Accessing the help files for built in functions
### accesing help on a specific topic
+ access help on spread() by typing ?spread
+ access help on library() by typing ?library


# M <a name="M"/>
## matrix
+ create matrix of elements
  - matrix(data = NA, nrow = 1, ncol = 1, byrow = FALSE,dimnames = NULL)
+ matrix with four elements 1,2,3,4 in 2 rows
  - matrix(1:4,2)

## mutate {dplyr}
+ add new column called status to table called passed
+ assign the value "passed" to each row in table
+ store the table with extra column in same table called passed
  -  passed <- passed %>% mutate(status = "passed") 


# N <a name="N"/>
## NA
+ Remove NA's from calculation
  - sum(ss06hid$VAL >= 24,na.rm = TRUE)


# S <a name="S"/>
## select
+ select(x,age) returns only column age

## Structure
+ display the dtructure of an arbitrary R object
+ provides useful summary on dataset
  - str(x)

## sum
+ sum(ss06hid$VAL >= 24)

## summary
+ summary of data
  - summary(x)
+ summary of subset of data (summary of column)
  - summary(x$age)


# T <a name="T"/>
## table
+ tabular summary of subset of data
  - summary(x$age)
+ prop.table returns table entries as fraction of the marginal table
  -  m <- matrix(1:4,2)
  -  m
  -  prop.table(m,1)

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


# U <a name="U"/>
## unique
+ eliminates duplicate rows


# V <a name="V"/>
## View
+ displays the dataset in tabular form
+ note the capital V
  - View(x)


# W <a name="W"/>
<a name="Workspace"/>
## Workspace
### list of variables
+ Type ls() to see a list of the variables in your workspace
  - type rm(list=ls()) to clear your workspace

<a name="write.csv"/>
## write.csv
### Write .csv file from data loaded in R
+ write.csv(by_package, file = "by_package.csv")

