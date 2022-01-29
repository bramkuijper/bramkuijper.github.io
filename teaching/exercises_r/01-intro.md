# Using loops to calculate sums and sums of squares
We often use loops to go over series of values and perform operations on them. While more advanced R users typically use techniques such as [vectorization](https://csgillespie.github.io/efficientR/programming.html#vectorised-code), or functions such as [`lapply()`](https://rdrr.io/r/base/lapply.html), using basic `for` loops is often the best thing to use when going over a series of values. Here we practice this by performing operations over a simple list of values.

## Printing values {#printEx}
Here we have the following list of values:



```r
# a list of values
my.list <- c(5,10,19,22,3,40,48)
```

Produce a `for` loop that uses the [`print()`](  https://www.rdocumentation.org/packages/base/versions/3.6.2/topics/print) function to print each value to the console, resulting in 
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
## A simple sum {#sum}
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
```

```
## [1] "Sum of odd numbers is 27. Sum of odd squares is 395."
```

Note the punctuation in the output above, which was
not there before and requires some changes in the `paste()`
statement. 

Hint: to find out whether a number is odd or even,
use the modulo operator `a %% b`. This gives the remainder of
the division `a/b`. For example,

```r
33 %% 3 
```

```
## [1] 0
```

```r
33 %% 2 
```

```
## [1] 1
```

```r
33 %% 5 
```

```
## [1] 3
```

```r
33 %% 10 
```

```
## [1] 3
```
