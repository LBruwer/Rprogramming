# Learning from Swirl (and other sources)

Contents:
## Click on the letter below to scroll to the same section

- [A](#A)  [B](#B)  [C](#C)  [D](#D)  [E](#E)  [F](#F)  [G](#G)  [H](#H)  [I](#I)  [J](#J)  [K](#K)  [L](#L)  [M](#M)  [N](#N)  [O](#O)  [P](#P)  [Q](#Q)  [R](#R)  [S](#S)  [T](#T)  [U](#U)  [V](#V)  [W](#W)  [X](#X)  [Y](#Y)  [Z](#Z)
- [Swirl](#Swirl)
- [R Packages](#Packages)

_______________________________________________________________________
-----------------------------------------------------------------------


### %>%
+ chaining commands - read as "then"
  - student_info <- students4 %>%
  
    select(id, name, sex) %>%
  
  - this stores the result of the select in student_info

### %/% "Div" or result
+ 
  -   

### %% "Mod" or remainder
+ 
  - 


# A <a name="A"/>
## apply() loop function
### lapply (list apply)
 - cls_list <- lapply(flags,class)
 - apply the class() function to each column of the flags dataset and store the result in a variable called cls_list
   To get a list containing the sum of each column of flag_colors, call the lapply() function with
   two arguments. The first argument is the object over which we are looping (i.e. flag_colors) and
   the second argument is the name of the function we wish to apply to each column (i.e. sum).
   
### sapply
+ average miles per gallon by number of cylinders
 - sapply(split(mtcars$mpg, mtcars$cyl), mean)

### arguments that a function can take - args()
+ args(list.files)
 - function (path = ".", pattern = NULL, all.files = FALSE, full.names = FALSE, 
    recursive = FALSE, ignore.case = FALSE, include.dirs = FALSE, 
    no.. = FALSE) 

### assign
+ transfer a variable from a function to the global environment
+ assign("AAA",newFile,envir = .GlobalEnv)
 - AAA is the variable

# B <a name="B"/>
### bind_rows
+ combining tables by row bind_rows(x,y)


# C <a name="C"/>
### class()

### unclass()

### collapse
+ `collapse` argument to the paste() function tells R that when we join together the elements of the 
   my_char character vector, we'd like to separate them with single spaces.
 - paste(my_char,collapse = " ")

# D <a name="D"/>
### data
+ data(mtcars)  (load data frame)

### date and time
+ strptime()
 - t3 <- "October 17, 1986 08:24"
 - strptime(t3, "%B %d, %Y %H:%M")
 - returns "1986-10-17 08:24:00 SAST"
+ difftime(Sys.time(), t1, units = 'days')
 - returns Time difference of 0.006077154 days

### download.file
+ download.file(fileUrl, destfile="./data/microdata.csv", )       (use method="curl" for mac)
    - fileurl <- "https://... "

### directory
+ make directory
 - mkdir("testdir")
+ set working directory
 - setwd("testdir") 

### dim
+ dimension of the variable
 - dim(x)


# F <a name="F"/>
### factor
+ factor(letters[1:20], labels = "letter")
 - produces letter1  letter2  letter3  lette4 etc up to letter20

### File and Directory Management
+ create new directory
  - dir.create("data")

### create file
+ file.create("mytest.R")

### rename file
+ file.rename("mytest.R", "mytest2.R")

### file copy
+ file.copy("mytest2.R" , "mytest3.R")

### full file path
+ file.path("mytest3.R")

### create sub directory
+ dir.create("testdir2/testdir3", recursive = TRUE)

### delete sub directory
+ unlink("testdir2", recursive = TRUE)

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

### list files in directory
+ list.files()

### check if file exists
+ file.exists("mytest.R")

### info on file in directory
+ file.info("mytest.R")

### grab specific items of info on file
+ file.info("mytest.R")$mode


# M <a name="M"/>
### matrix
+ create matrix of elements
  - matrix(data = NA, nrow = 1, ncol = 1, byrow = FALSE,dimnames = NULL)
+ matrix with four elements 1,2,3,4 in 2 rows
  - matrix(1:4,2)

### memory occupied
+ object.size(x)
 - returns 644232 bytes

### mutate {dplyr}
+ add new column called status to table called passed
+ assign the value "passed" to each row in table
+ store the table with extra column in same table called passed
  -  passed <- passed %>% mutate(status = "passed") 


# N <a name="N"/>
### NA
+ Remove NA's from calculation
  - sum(ss06hid$VAL >= 24,na.rm = TRUE)
+ remove NA's from vector x and assign to vector y
 - y <- x[!is.na(x)]

### names
+ column names
 - cnames <- c("patient", "age", "weight","bp", "rating", "test")
 - colnames(my_data) <- cnames

### now
+ now()
  - hour, minute


# P <a name="P"/>
### paste()
+ join elements of character vector into continuous string
 - paste(my_char,collapse = " ")
 - paste(LETTERS, 1:4, sep = "-")

### plot
+ data(cars)
+ plot(cars) (plot is short for scatterplot)
+ plot(x = cars$speed, y = cars$dist, xlab = "Speed")
 - label of x axis is now "speed"
 - plot(cars,col=2)  (changes plot colour to red)
 - plot(cars,xlim =c(10,15)) (limit x axis 10 -15)
+ par (graphical paramenters)
+ symbols change
 - plot(cars,pch = 2) (triangles)
+ ggplot
+ boxplot
 - boxplot(formula = mpg ~ cyl , data = mtcars)
+ hist
 - hist(mtcars$mpg)


# R <a name="R"/>
### rattle()
+ connect to SQL 
 - library(RODBC)
 - DSN setup ODBC setup in Windows

### range
+ returns the minimum and maximum of its first argument

### read.csv()
+ reads .csv (and comma seperated .txt ) files
+ read.csv(file_list[i],header = FALSE,skip=1)
 - header = FALSE skips the header
 - skip = 1 ignores the 1st data row
+ read.csv("your_file")
+ train_url <- "http://s3.amazonaws.com/assets.datacamp.com/course/Kaggle/train.csv"
 - 
train <- read.csv(train_url)

### recoding variables
+ Assign the label "high" to mpgcategory where mpg is greater than or equal to 20

+ mtcars2$mpgcategory[mtcars2$mpg >= 20] <- "high"


### repeat
+ rep(0, times = 40)
+  rep(c(0, 1, 2), times = 10)


# S <a name="S"/>

### sample()
+ my_data <- sample(c(y,z),100)
+ rep(c(0, 1, 2), each = 10)

### select
+ select(x,age) returns only column age

### structure
+ display the dtructure of an arbitrary R object
+ provides useful summary on dataset
  - str(x)

### SQL {RODBC}
+ library("RODBC")
+ library(RODBC)
 - channel <- odbcConnect("jhbbi",uid="ReportUser",pwd="ReportUser")
 - ChannelHierarchy <- sqlQuery(channel,"SELECT * FROM DW.dim.PartnerListNew")
 - close(channel)

+ sqldf {sqldf}


### subsets
+ which()
 - which(ints>7)
 - which(ints <= 2)
+ any()
 - any(ints<0)
+ all()
 - all(ints>0)
+ subset of matrix with 2 columns filtered
 - subset(x, Ozone > 31 & Temp > 90)

### sum
+ sum(ss06hid$VAL >= 24)

### summary
+ summary of data
  - summary(x)
+ summary of subset of data (summary of column)
  - summary(x$age)


# T <a name="T"/>
### table
+ table cross-classifying factors of counts
 - table(plants$Active_Growth_Period)
+ tabular 
+ tabular summary of subset of data
  - summary(x$age)
+ prop.table returns table entries as fraction of the marginal table
  -  m <- matrix(1:4,2)
  -  m
  -  prop.table(m,1)

+ table data frame {dplyr}
 - tbl_df
    - select()  subset of columns
    - filter()  subset of rows
    - arrange()
    - mutate()
    - summarize()
 - chaining %>%
    - cran %>%
      select(ip_id, country, package, size) %>%
      mutate(size_mb = size / 2^20) %>%          add column size_mb derived from existing column size
      filter(size_mb <= 0.5) %>%                 filter results by size_mb <= 0.5
      arrange(desc(size_mb))                     sort descending by size_mb

### test if vector contains element
+ v <- c('a','b','c','e')
 - 'b' %in% v
 - returns TRUE
+ state %in% state.list
 

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

### unzip
+ unzip("data/activity.zip")


# V <a name="V"/>
### View
+ displays the dataset in tabular form
+ note the capital V
  - View(x)

### viewinfo()


# W <a name="W"/>
<a name="Working Directory"/>
### Set Working Directory
+ setwd("~/")
+ setwd("J:/01 Training Courses")
+ setwd("J:/01 Training Courses/Coursera/04 Exploratory Data Analysis/Data")

<a name="Workspace"/>
### Workspace
### list of variables
+ type ls() to see a list of the variables in your workspace
  - type rm(list=ls()) to clear your workspace

<a name="write.csv"/>
### write.csv
### write .csv file from data loaded in R
+ write.csv(by_package, file = "by_package.csv")


# X <a name="X"/>

# Y <a name="Y"/>

# Z <a name="Z"/>








# swirl <a name="swirl"/>
<a name="Swirl"/>
### Swirl
+ library(swirl)
+ install_from_swirl("R Programming")
+ install_from_swirl("Getting and Cleaning Data")
+ install_from_swirl("Exploratory Data Analysis")
+ install_from_swirl("Data Analysis")
+ install_from_swirl("Regression Models")
+ install_from_swirl("Open Intro")
+ install_from_swirl("Statistical Inference")

+  uninstall_course("Course Name Here") 

| When you are at the R prompt (>):

| -- Typing skip() allows you to skip the current question.  
| -- Typing play() lets you experiment with R on your own; swirl will ignore what you do...  
| -- UNTIL you type nxt() which will regain swirl's attention.  
| -- Typing bye() causes swirl to exit. Your progress will be saved.  
| -- Typing main() returns you to swirl's main menu.  
| -- Typing info() displays these options again.  


# packages <a name="packages"/>
<a name="R Packages"/>
### R Packages
## install.packages("package name here")
### dplyr
### ggplot2
### swirl
### knitr
### data.table
### rattle
### rpart.plot
### RColorBrewer

### install.packages("RODBC",type = "source")
### install.packages("sqldf")

### ? Rccp




