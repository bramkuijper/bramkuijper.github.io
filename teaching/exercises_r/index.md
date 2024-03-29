--- 
title: "Various exercises on programming in R"
author: "Bram Kuijper"
date: "2022-01-28"
site: bookdown::bookdown_site
output: bookdown::gitbook
documentclass: book
bibliography: ["refsR.bib"]
biblio-style: apalike
link-citations: yes
description: "A brief set of exercises on control flow and loops in R"
---

# Introduction

Here a small selection of problems to get some practical exposure to R programming. Some of these exercises may be quite relevant to one's work, other may be less so. However, relevance to one's work is not a really good criterion here; we simply want to practice problem solving.

## Prior knowledge about R
This set of exercises assumes you already have a reasonable understanding of the R basics. Here a bunch of different sources that provide an overview of the R basics:
 
* Chapters 1-8 of the book *The Book of R* [@Davies2016], which is available in UExeter's library [here](https://encore.exeter.ac.uk/iii/encore/record/C__Rb3554370){target="_blank"} 
* [An introduction to R](https://cran.r-project.org/doc/manuals/r-release/R-intro.html){target="_blank"} freely available from the R website.
* Chapter 2 of the book *The R Book* [@Crawley2013], which is available in UExeter's library [here](https://encore.exeter.ac.uk/iii/encore/record/C__Rb3361719){target="_blank"}
* Chapter 1-7 of the book *The Art of R Programming* [@Matloff2011], which is available in UExeter's library [here](https://encore.exeter.ac.uk/iii/encore/record/C__Rb3509192){target="_blank"}

One should not search for pdfs of these books online.

### Finding help
Next to googling everything you don't understand, you can also find help using the [`?`](https://stat.ethz.ch/R-manual/R-devel/library/utils/html/Question.html){target="_blank"} command in R's built-in help pages. For example, you can use the `?` preceding a certain function or variable. For example, in case we want more information about R's [`str()`](https://stat.ethz.ch/R-manual/R-devel/library/utils/html/str.html) function, we simply type

```r
?str
```
Obviously, next to R's built-in help pages, search engines are your friend when you hunt for examples. 

**Pro-tip: use quotation marks `""` when consulting help for operators and weird characters** For operators and things with weird characters, using the  `?` help function may not bring you very far. For example, let's say you are interested in finding out about R's [`%in%`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/match.html) matching operator:

```r
?%in%
## Error: <text>:1:2: unexpected SPECIAL
## 1: ?%in%
##      ^
```

Clearly, R chokes on the `%` character. What now? Easy, just use quotes:

```r
?"%in%"
```

### Different types of variables
You know about variables and different types of data such as `character`, `logical`. Also,you know about different data structures such as [`c()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/c.html){target="_blank"} (vectors), [`data.frame`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/data.frame.html){target="_blank"}s and [`list`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/list.html){target="_blank"}s. Finally, you know that the  [`typeof()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/typeof.html){target="_blank"} function can be used to find out what data is contained in a data type. Similarly, also the [`str()`](https://stat.ethz.ch/R-manual/R-devel/library/utils/html/str.html){target="_blank"} helps you to find out more about the structure of a data type. Please see [here](https://swcarpentry.github.io/r-novice-inflammation/13-supp-data-structures/){target="_blank"} for a fantastic overview of the different data types and key data structures.

### Operators
Please click the corresponding links if you do not know about [arithmetic operators](https://stat.ethz.ch/R-manual/R-devel/library/base/html/Arithmetic.html){target="_blank"} such as `*` (multiplication), `^` (power), `%%` (modulo). The same goes for [logical operators](https://stat.ethz.ch/R-manual/R-devel/library/base/html/Logic.html){target="_blank"} such as `||` (which is the `OR` operator) and [relational operators](https://stat.ethz.ch/R-manual/R-devel/library/base/html/Comparison.html){target="_blank"} such as `>=` (which is the greater-than-or-equal-operator). See [Chapter 4](https://bookdown.org/swen/R_for_Everyone/L03.html#r-as-a-calculator){target="_blank"} for a brief overview. 

### Control flow
Things like `if`-`else` statements and [`ifelse()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/ifelse.html){target="_blank"} functions should be understood. Read the freely available [Chapter 5](https://adv-r.hadley.nz/control-flow.html){target="_blank"} from [@Wickham2019] for more information, or chapter 7 of [@Matloff2011] 

### Sizes of things 
To use loops, knowing the sizes of things in R is important. Hence, you know how to obtain the [`length()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/length.html){target="_blank"} of a vector, or the number of characters in a string of text using [`nchar()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/nchar.html){target="_blank"}. You also know how to obtain the number of rows and columns of a `data.frame`, using [`nrow()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/nrow.html){target="_blank"},  [`ncol()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/ncol.html){target="_blank"} or its dimensions using [`dim()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/dim.html){target="_blank"}. 

## Selecting subsets of your data
You know the difference between `iris[,1]`, `iris[1,]` and `iris[1,1]`? See [Chapter 4](https://adv-r.hadley.nz/subsetting.html){target="_blank"} for a great overview of how to subset your data in different ways.

### Loop structures
You will need to have read about `for`-loops and potentially also about [`switch()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/switch.html){target="_blank"} statements. Check out chapter 7 of [@Matloff2011], chapter 21 of [@Wickham2017] (available online) or check online for videos on these topics. For example, using the search terms `for loops in R` provides a bunch of great videos. 

## Some additional coding tips:

### Don't ignore the links and hints
 Sometimes there are hints provided in the exercises, for example:
"You can do this by using the [`paste()`](https://stat.ethz.ch/R-manual/R-patched/library/base/html/paste.html){target="_blank"} function", which involves
you reading the documentation on this function and trying
some of the provided examples in the documentation. I typically provide hyperlinks to the documentation, which is why the [`paste()`](https://stat.ethz.ch/R-manual/R-patched/library/base/html/paste.html) function here is given in blue. Click on them and read them. Please do.

### Try out examples for yourself
When reading a book, try the code examples and snippets for yourself, by typing them out (don't copy-paste them, unless it is a massive amount of code). Only by typing out do you see what's going on and will you start to memorize the different coding constructs. Moreover, you are bound to make occasional mistakes! And mistakes are good, as the earlier you learn how to hunt for coding errors and solving mistakes the better.

### Search enginges are your friend
Search engines are your friend. If some function or construct is used that is new to one, google what it is about. Say, one encounters the statement 

```r
means <- apply(X=cars,MARGIN=2,FUN=mean)
```
and one does not know what the [`apply`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/apply.html){target="_blank"} statement is about or what the `cars` variable is about, I'd immediately search for `apply r` or `cars r`. 

### Comment your code
Always try to briefly comment each statement (or group of statements), using `#`. 

```r
# select even numbers
even_odd <- c(1,2,3,4,5,6,7,8) %% 2 == 0
```

### Keep an error record
Try to keep a record of all the main error messages you encounter, so that you build a record of different error messages and how they have eventually been resolved. This serves as a great lookup tool for recurring errors. 

An entry in my error record reads, for example:

```r
apply(X=cars,MARGIN=2,FUN=mean())
## Error in mean.default(): argument "x" is missing, with no default
```
This error occurs because the supplied `mean()` function used to calculate means of the different columns is provided with parentheses `()`. However, in order for this function to actually calculate means of each column, you simply need to provide the function name `mean` without the parentheses, or:

```r
apply(X=cars,MARGIN=2,FUN=mean)
## speed  dist 
## 15.40 42.98
```

### Find out the root of errors using `traceback()`
If you stumble upon an error, use R's [`traceback()`](https://stat.ethz.ch/R-manual/R-devel/library/base/html/traceback.html){target="_blank"} function to find the root cause. As `traceback()` can produce a lot of garbage, it may help to reduce the amount of output, for example by stating `traceback(max.lines=5)`.

### Inspect values using `print()` or use R's debugger
When you have just started to code in R, use as many [`print()`](https://stat.ethz.ch/R-manual/R-patched/library/base/html/print.html){target="_blank"} statements as possible, to obtain information about the state of your program and the values of your variables. When you become more experienced, you can start to inform yourself about R's very handy debugging tools that can do all the variable inspection work for you. Read more about R debugging in the freely available [chapter 22](https://adv-r.hadley.nz/debugging.html) of [@Wickham2019].
