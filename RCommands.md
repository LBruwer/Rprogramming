# A short list of the most useful R commands

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


# Input and display
## read files with labels in first row
read.table(filename,header=TRUE)           #read a tab or space delimited file
read.table(filename,header=TRUE,sep=',')   #read csv files

## x <- c(1,2,4,8,16 )                        ### create a data vector with specified elements
y <- c(1:10)                                  #create a data vector with elements 1-10
n <- 10
x1 <- c(rnorm(n))                             #create a n item vector of random normal deviates
y1 <- c(runif(n))+n                           #create another n item vector that has n added to each random uniform distribution
z <- rbinom(n,size,prob)                      #create n samples of size "size" with probability prob from the binomial
vect <- c(x,y)                                #combine them into one vector of length 2n
mat <- cbind(x,y)                             #combine them into a n x 2 matrix
mat[4,2]                                   #display the 4th row and the 2nd column
mat[3,]                                    #display the 3rd row
mat[,2]                                    #display the 2nd column
subset(dataset,logical)                    #those objects meeting a logical criterion
subset(data.df,select=variables,logical)   #get those objects from a data frame that meet a criterion
data.df[data.df=logical]                   #yet another way to get a subset
x[order(x$B),]                             #sort a dataframe by the order of the elements in B
x[rev(order(x$B)),]                        #sort the dataframe in reverse order 

browse.workspace                           #a Mac menu command that creates a window with information about all variables in the workspace
