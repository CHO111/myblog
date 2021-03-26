---
title: post
date: 2021-03-23 17:02:05
tags:
---
```r
# 1번문제
library(ggplot2)
ggplot(iris, aes(x = Sepal.Length, 
                 y = Sepal.Width,
                 size = Petal.Length,
                 colour = "red"#Species
                 )) +
 geom_point()
```

![](/image/unnamed-chunk-1-1.png)<!-- -->