---
title: 데이터 변환 정리
date: 2021-03-23 17:25:01
tags:
    number_sections: true
    toc: true
    toc_depth: 3
---
# 1. 소개
데이터 시각화는 통찰력 생성에 중요한 도구지만 정확한 형식으로 데이터를 얻기 힘들기 떄문에 데이터 변환을 이용한다.

# 1.1 전제조건
tidyverse의 또 다른 핵심 멤버 인 dplyr 패키지를 사용하는 방법에 초점을 맞춘 정리입니다. 
nycflights13 패키지의 데이터를 사용하여 데이터 변환에 대한 정리를 진행하며 
ggplot2를 사용하여 데이터를 이해하는 데 도움을 줄 것입니다.
```{r}
library(nycflights13)
library(tidyverse)
```

## 1.2 nycflights13
이 데이터는 2013년 뉴욕에서 출발한 항공편의 데이터입니다.
```{r}
flights
#> # A tibble: 336,776 x 19
#>    year month   day dep_time sched_dep_time dep_delay arr_time sched_arr_time
#>   <int> <int> <int>    <int>          <int>     <dbl>    <int>          <int>
#> 1  2013     1     1      517            515         2      830            819
#> 2  2013     1     1      533            529         4      850            830
#> 3  2013     1     1      542            540         2      923            850
#> 4  2013     1     1      544            545        -1     1004           1022
#> 5  2013     1     1      554            600        -6      812            837
#> 6  2013     1     1      554            558        -4      740            728
#> # … with 336,770 more rows, and 11 more variables: arr_delay <dbl>,
#> #   carrier <chr>, flight <int>, tailnum <chr>, origin <chr>, dest <chr>,
#> #   air_time <dbl>, distance <dbl>, hour <dbl>, minute <dbl>, time_hour <dttm>
```
데이터 프레임의 아랫줄에 <>안에 들어가는 단어는 각변수의 데이터 유형을 뜻합니다.
* int -> 정수를 의미
* dbl -> 실수를 의미
* chr -> 문자열 의미
* dttm -> 날짜-시간 의미

## 1-3 dplyr의 기본사항
dplyr 함수에는 대부분의 데이터 조작 문제를 해결할 수 있는 5가지 주요함수가 있습니다.
![](/image/Data_transformation1.jpg)
sdfsdf