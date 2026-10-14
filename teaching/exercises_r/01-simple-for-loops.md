# Using loops to calculate sums and sums of squares
We often use loops to go over series of values and perform operations on them. While more advanced R users typically use techniques such as [vectorization](https://csgillespie.github.io/efficientR/programming.html#vectorised-code), or functions such as [`lapply()`](https://rdrr.io/r/base/lapply.html), using basic `for` loops is often the best thing to use when going over a series of values. Here we practice this by performing operations over a simple list of values.


## Exercise: printing elements from a vector {#printEx}
Here we have the following vector of values:



```r
# a list of values
my.list <- c(5,10,19,22,3,40,48)
```

Produce a `for` loop that uses the [`print()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/print.html){target="_blank"} function to print each value to the console, resulting in 
the following output:

```
## [1] 5
## [1] 10
## [1] 19
## [1] 22
## [1] 3
## [1] 40
## [1] 48
```

## Exercise: printing every $n$th row from a `data.frame`
Let us use the built-in `cars` dataset. Use a `for` loop to go over the rows of this `data.frame` and then use the [`print()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/print.html){target="_blank"} function to print every 10th row, as in

```
##   speed dist
## 1     4    2
##    speed dist
## 11    11   28
##    speed dist
## 21    14   36
##    speed dist
## 31    17   50
##    speed dist
## 41    20   52
```

## Exercise: summing a vector {#sum}
Produce a single `for` loop to calculate the sum of `my.list`
in exercise \@ref(printEx). This is chiefly for the sake of 
practice, as in reality we would use the [`sum()`](https://rdrr.io/r/base/sum.html)
function for this. The only output of your script should be:

```
## [1] "The sum of the list is 147"
```
which can be done using the functions [`print()`](  https://www.rdocumentation.org/packages/base/versions/3.6.2/topics/print)
and, in particular, [`paste()`](https://www.rdocumentation.org/packages/base/versions/3.6.2/topics/paste) which allows you to concatenate strings (pieces of text) and numbers into one sentence.

## Sums of squares {#sumSq}
Now copy-paste and modify the code from exercise \@ref(sum)
to calculate both the sum
and the sum of squares within one and the same `for` loop.
Calculating the sum of squares is the same as first squaring each 
numbers and then summing these squares, i.e., $5\times 5 + 10 \times 10 + \cdots + 48 \times 48$.

The program should have no output, other than the
following message at the end: 


```
## [1] "The sum is 147 and the sum of squares is 4883"
```
and again, this can be realized using the functions `print()` and `paste()`.

## Sum only if larger than $x$
Copy-paste the code from exercise \@ref(sumSq)
and use an `if`-statement 
to calculate the sum and 
the sum of squares for those numbers in the list above
that are greater or equal than $x=10$. Other numbers
can be ignored. The resulting message should now be:

```
## [1] "The sum is 139 and the sum of squares is 4849"
```

## Separate sums for odd and even numbers
Copy-paste the code from exercise \@ref(sumSq) 
and modify it to calculate sums and 
sums of squares 
for odd and even numbers separately. 
Do this using an `if`-`else`
statement. The resulting code should print
the following two messages:

```
## [1] "Sum of even numbers is 120. Sum of even squares is 4488."
## [1] "Sum of odd numbers is 27. Sum of odd squares is 395."
```

Note the punctuation in the output above, which was
not there before and requires some changes in the `paste()`
statement. 

**Hint:** to find out whether a number is odd or even,
use the modulo operator `a %% b`. This gives the remainder of
the division `a/b`. For example,

```r
33 %% 3 
## [1] 0
33 %% 2 
## [1] 1
33 %% 5 
## [1] 3
33 %% 10 
## [1] 3
```


## Produce a vector of cumulative values 
Say, you have a vector of values, called `a.vec`. From this vector, one can produce another vector, called a cumulative vector, which is often used to develop sampling distributions. The $i$th index of such a vector contains the sum of elements from element $1$ to $i$. For example, for the following vector 

```r
a.vec <- c(5,9,1,3,12,8,50,82,1,9,2,7)
```
the corresponding cumulative vector should contain the following sequence of values:

```
##  [1]   5  14  15  18  30  38  88 170 171 180 182 189
```

1. Develop code that produces a cumulative vector for the vector `a.vec` above, where the cumulative vector should be contained in the variable `cumul.vec`. The variable `cumul.vec` should be initialized before the start of the `for`-loop as an `NA`-filled vector of the same length as `a.vec`.
2. Now, we assign `a.vec <- iris[,1]`. Without any further changes to your code, it should now fill `cumul.vec` with cumulative values for this new version of `a.vec`. Output should now be:

```
##   [1]   5.1  10.0  14.7  19.3  24.3  29.7  34.3  39.3  43.7  48.6  54.0  58.8
##  [13]  63.6  67.9  73.7  79.4  84.8  89.9  95.6 100.7 106.1 111.2 115.8 120.9
##  [25] 125.7 130.7 135.7 140.9 146.1 150.8 155.6 161.0 166.2 171.7 176.6 181.6
##  [37] 187.1 192.0 196.4 201.5 206.5 211.0 215.4 220.4 225.5 230.3 235.4 240.0
##  [49] 245.3 250.3 257.3 263.7 270.6 276.1 282.6 288.3 294.6 299.5 306.1 311.3
##  [61] 316.3 322.2 328.2 334.3 339.9 346.6 352.2 358.0 364.2 369.8 375.7 381.8
##  [73] 388.1 394.2 400.6 407.2 414.0 420.7 426.7 432.4 437.9 443.4 449.2 455.2
##  [85] 460.6 466.6 473.3 479.6 485.2 490.7 496.2 502.3 508.1 513.1 518.7 524.4
##  [97] 530.1 536.3 541.4 547.1 553.4 559.2 566.3 572.6 579.1 586.7 591.6 598.9
## [109] 605.6 612.8 619.3 625.7 632.5 638.2 644.0 650.4 656.9 664.6 672.3 678.3
## [121] 685.2 690.8 698.5 704.8 711.5 718.7 724.9 731.0 737.4 744.6 752.0 759.9
## [133] 766.3 772.6 778.7 786.4 792.7 799.1 805.1 812.0 818.7 825.6 831.4 838.2
## [145] 844.9 851.6 857.9 864.4 870.6 876.5
```

