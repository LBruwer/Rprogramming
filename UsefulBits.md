# Learning from Swirl (and other sources)

Contents:
## Click on the letter below to scroll to the same section

- [A](#A)  [B](#B)  [C](#C)  [D](#D)  [E](#E)  [F](#F)  [G](#G)  [H](#H)  [I](#I)  [J](#J)  [K](#K)  [L](#L)  [M](#M)  [N](#N)  [O](#O)  [P](#P)  [Q](#Q)  [R](#R)  [S](#S)  [T](#T)  [U](#U)  [V](#V)  [W](#W)  [X](#X)  [Y](#Y)  [Z](#Z)

_________________________________________________________________________
-------------------------------------------------------------------------

### %>%
+ chaining commands - read as "then"
  - student_info <- students4 %>%
  
    select(id, name, sex) %>%
  
  - this stores the result of the select in student_info

### %/%
+ 
  -   

### %%
+ 
  - 


# A <a name="A"/>

# B <a name="B"/>
### bind_rows
+ combining tables by row bind_rows(x,y)


# C <a name="C"/>
### class


# D <a name="D"/>
### download.file
+ download.file(fileUrl, destfile="./data/microdata.csv", method="curl")
  - fileurl <- "https://... "


# F <a name="F"/>
### File and Directory Management
+ create new directory
  - dir.create("data")


# H <a name="H"/>
<a name="Help"/>
### Accessing the help files for built in functions
### accesing help on a specific topic
+ access help on spread() by typing ?spread
+ access help on library() by typing ?library
+ access help on package lubridate by typing help(package = lubridate)


# L <a name="L"/>
### locale - date and region settings
+ Sys.getlocale("LC_TIME")


# M <a name="M"/>
### matrix
+ create matrix of elements
  - matrix(data = NA, nrow = 1, ncol = 1, byrow = FALSE,dimnames = NULL)
+ matrix with four elements 1,2,3,4 in 2 rows
  - matrix(1:4,2)

### mutate {dplyr}
+ add new column called status to table called passed
+ assign the value "passed" to each row in table
+ store the table with extra column in same table called passed
  -  passed <- passed %>% mutate(status = "passed") 


# N <a name="N"/>
### NA
+ Remove NA's from calculation
  - sum(ss06hid$VAL >= 24,na.rm = TRUE)


### now
+ now()
  - hour, minute


# S <a name="S"/>
### select
+ select(x,age) returns only column age

### Structure
+ display the dtructure of an arbitrary R object
+ provides useful summary on dataset
  - str(x)

### sum
+ sum(ss06hid$VAL >= 24)

### summary
+ summary of data
  - summary(x)
+ summary of subset of data (summary of column)
  - summary(x$age)


# T <a name="T"/>
### table
+ tabular summary of subset of data
  - summary(x$age)
+ prop.table returns table entries as fraction of the marginal table
  -  m <- matrix(1:4,2)
  -  m
  -  prop.table(m,1)

### today {lubridate}
+ today()
  - weekday wday()
  - day, year, month
+ ymd(), dmy(), hms(), ymd_hms()
  - ymd("1989 may 17") returns "1989-05-17 UTC"
  - mdy("March 12 1975") returns "1975-03-12 UTC"
  - dmy(25081985) returns "1985-08-25 UTC"
+ update()
  - this_moment, hours = 8, minutes = 34, seconds = 55)
+ now()
  - nyc <- now("America/New_York")  ("2015-02-19 07:06:11 EST")
  - nyc + days(2) returns 
  - http://en.wikipedia.org/wiki/List_of_tz_database_time_zones
+ time zone
  - with_tz()
  - arrive <- with_tz(arrive, "Asia/Hong_Kong")
+ elapsed time
  - new_interval()  - how_long <- new_interval(last_time,arrive)
  - as.period(how_long) returns "6y 8m 3d 22H 24M 11.6900999546051S"
+ stopwatch()
  - how long been working

<a name="tidy"/>
### tidy
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
### unique
+ eliminates duplicate rows


# V <a name="V"/>
### View
+ displays the dataset in tabular form
+ note the capital V
  - View(x)


# W <a name="W"/>
<a name="Workspace"/>
### Workspace
### list of variables
+ type ls() to see a list of the variables in your workspace
  - type rm(list=ls()) to clear your workspace

<a name="write.csv"/>
### write.csv
### write .csv file from data loaded in R
+ write.csv(by_package, file = "by_package.csv")

