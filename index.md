---
title       : Rock-Scissors-Paper
subtitle    : 
author      : Uli Zellbeck
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Overview

This is an awesome presentation of Rock-Scissors-Paper.
With this application you will no longer have any problems what to do with your free time.
In this presentation you will see the magic behind this application.

--- .class #id 

## How it works (technically) #1

The R Code for ui.R is simple:
If you choose one item it is decoded into a number. For instance "Rock"" is decoded into 1.


```r
input <- 1
```

On the computer side a sample number is generated:


```r
x <- sample(1:3,1+as.numeric(input)-as.numeric(input))
```

So here is the clue for sampling:
As it always includes the input variable a new sample is reactively generated.

--- .class #id 

## How it works (technically) #2

What it simply does is comparing both numbers and then calculating the result:


```r
  if (x==1 && as.numeric(input)==1) y <- "Rock: It's a draw!"
  if (x==2 && as.numeric(input)==1) y <- "Paper: You lose!"
  if (x==3 && as.numeric(input)==1) y <- "Scissors: You win!"
  y
```

```
## [1] "Rock: It's a draw!"
```

--- .class #id

Thank you for your patience.
If you want to see this amazing application visit:

 [myAmazingApp](http://ulizellbeck.shinyapps.io/assignment/)
