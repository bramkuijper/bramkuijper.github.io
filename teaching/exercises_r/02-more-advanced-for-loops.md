# Slightly more advanced for loops
In this set of exercises we will look at slightly more complicated for loops. 


## Exercise: a list of random letters
The `LETTERS` 


## Exercise: changes in state over time
In many biological models, we model environments that change between two states, `0` and `1`. For example, these environments may represent a dry vs a hot environment. Let $\phi$ reflect the probability that an environment changes from one state to another.







## Exercise: select columns of a `data.frame` containing floating-point numbers
Data types like [`data.frames`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/data.frame.html) and [`tibbles`](https://tibble.tidyverse.org/) are collections of variables ordered in rows and columns, like a spreadsheet. Take for example the `Cars93` `data.frame` from R's `MASS` package, which we inspect with the [`str()`](https://stat.ethz.ch/R-manual/R-devel/library/utils/html/str.html) command:

```r
library("MASS")
str(Cars93)
## 'data.frame':	93 obs. of  27 variables:
##  $ Manufacturer      : Factor w/ 32 levels "Acura","Audi",..: 1 1 2 2 3 4 4 4 4 5 ...
##  $ Model             : Factor w/ 93 levels "100","190E","240",..: 49 56 9 1 6 24 54 74 73 35 ...
##  $ Type              : Factor w/ 6 levels "Compact","Large",..: 4 3 1 3 3 3 2 2 3 2 ...
##  $ Min.Price         : num  12.9 29.2 25.9 30.8 23.7 14.2 19.9 22.6 26.3 33 ...
##  $ Price             : num  15.9 33.9 29.1 37.7 30 15.7 20.8 23.7 26.3 34.7 ...
...
```

Sometimes, we would like to select certain columns from such a `data.frame`, dependent on a particular condition. Hence the current exercises:

Select only those columns from `Cars93` which contain floating-point numbers, such as `6.5` or `1e-03`. Use a `for`-loop to loop over the columns of `Cars93` to select those columns 




To progress with the exercise, here a couple of hints:

### Hint 1: data types
The way to find out whether a column of a `data.frame` contains floating-point numbers is to use the [`typeof()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/typeof.html) function. Let us compare two different columns from the `Cars93` dataset, for example: 

```r
typeof(Cars93[,"Min.Price"])
## [1] "double"
typeof(Cars93[,"MPG.city"])
## [1] "integer"
```

where `double` reflects that the `Min.Price` column contains floating-point numbers, whereas `integer` reflects that the `MPG.city` column contains integers. 


### Hint 2: data.frame dimensions
To loop through the columns of the `data.frame`, you need to find out the dimensions. The total number of columns (or rows) can be obtained by [`ncol()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/nrow.html){target="_blank"} (or [`ncol()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/nrow.html){target="_blank"}).

### Hint 3: select columns based on a vector
To select multiple columns in a `data.frame` (if you forgot about column and row selection, see page 66 and beyond in [@Matloff2011]), you can use a vector with numbers:

```r
# make a vector containing the column numbers that you want to select
# in this case: column 1, column 2, column 4
column.select <- c(1,2,4)
Cars93[,column.select]
##     Manufacturer          Model Min.Price
## 1          Acura        Integra      12.9
## 2          Acura         Legend      29.2
## 3           Audi             90      25.9
## 4           Audi            100      30.8
...
```


## Nested for loops
In this part of the exercises, we will be looking at nested `for` loops

## Parameter combinations






