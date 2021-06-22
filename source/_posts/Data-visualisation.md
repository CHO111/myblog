---
title: 데이터 시각화
date: 2021-03-29 16:40:15
tags: R
categories: R
---
# 1. 소개
데이터 시각화는 데이터를 그림이나 그래프를 통해 시작적으로 표현하는 모든 과정입니다.
시각화는 단순히 멋있게 만드는것을 떠나 데이터를 쉽게 보고 이해할 수 있도록 도와줍니다.

## 1.1. 전제 조건
R에는 그래프를 만들기위한 여러 시스템이 있지만 그중하나인 ggplot2에 중점을 두고 정리를 해볼려고 합니다.
* tidyverse 패키지는 R에서 데이터를 정제하고 다루는 패키지를 묶어서 하나의 패키지로 만든것이다.
    - 설치방법
    ```
    install.packages("tidyverse") -> 패키지 설치
    library(tidyverse) -> 패키지 불러오기
    ```

# 2. 첫 단계
ggplot2 에 내장된 샘플데이터를 이용해 분석을 진행해보자.

## 2.1. mpg 데이터 프레임
mpg데이터는 ggplot2 에 내장된 샘플데이터로 자동차모델에 대한 정보입니다.
```{r}
mpg
#> # A tibble: 234 x 11
#>   manufacturer model displ  year   cyl trans      drv     cty   hwy fl    class 
#>   <chr>        <chr> <dbl> <int> <int> <chr>      <chr> <int> <int> <chr> <chr> 
#> 1 audi         a4      1.8  1999     4 auto(l5)   f        18    29 p     compa…
#> 2 audi         a4      1.8  1999     4 manual(m5) f        21    29 p     compa…
#> 3 audi         a4      2    2008     4 manual(m6) f        20    31 p     compa…
#> 4 audi         a4      2    2008     4 auto(av)   f        21    30 p     compa…
#> 5 audi         a4      2.8  1999     6 auto(l5)   f        16    26 p     compa…
#> 6 audi         a4      2.8  1999     6 manual(m5) f        18    26 p     compa…
#> # … with 228 more rows
```
위 데이터에서 ggplot로 시각화시킬 변수는 displ(엔진크기), hwy(자동차연비)로 하겠습니다.

## 2.2. ggplot 생성
ggplot를 생성하는 코드입니다 
```{r}
ggplot(data = mpg) + 
  geom_point(mapping = aes(x = displ, y = hwy))
```
![](/image/image2/Rplot01.png)
* ggppot(data = mpg) 를 실행하면 mpg데이터를 기반으로한 빈그래프가 생성됩니다.
    - 생성된 빈그래프에 하나 이상의 레이어를 추가해서 그래프를 완성시켜줍니다.
* geom_point()는 점 레이어를 추가하여 산점도를 생성해서 위 사진과 같은 완성된 그래프가 나오게됩니다.

### 2.2.1 미적매핑
* ggplot2의 각 geom 함수는 mapping 인수를 받습니다. 이는 데이터의 변수가 시각적 속성에 매핑되는 방식을 정의합니다.
    - mapping인수는 항상 미학요소(aesthetics, aes) 에 x축과 y축에 매핑되는 변수를 지정하고 크기 형태 색상등을 매핑할수 있습니다.
    ```{r}
      ggplot(data = mpg) + 
      geom_point(mapping = aes(x = displ, y = hwy, color = class))
    ```
      ![](/image/Rplot.png)
    
위 사진은 첫번쨰 산점도그래프의 자료에서 자동차의 등급별생상을 나타낸 자료입니다 .      

# 3. 막대 그래프
데이터를 막대그래프로 표현하기위해선 geom_bar()를 씁니다 
예시로 내장된 샘플데이터 diamonds를 사용하여 막대그래프를 표현해보겠습니다.
```{r}
ggplot(data = diamonds) + 
geom_bar(mapping = aes(x = cut))
```
![](/image/image2/Rplot02.png)
위 사진은 샘플데이터 diamonds 의 품질 및 개수를 막대 그래프로 나타낸 것 입니다.