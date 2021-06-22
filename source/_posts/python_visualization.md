---
title: 파이썬 시각화 실습
date: 2021-04-07 11:46:18
tags: python
categories: Python
---
## 라이브러리 호출
```python
## 필요한 라이브러리들을 불러옵니다.
import matplotlib.pyplot as plt 
from matplotlib.ticker import (MultipleLocator, AutoMinorLocator, FuncFormatter)
import seaborn as sns
import numpy as np
```
<br>

## 시각화코드 함수생성
```python
# 시각화코드 함수로 생성 시각화코드 함수로 생성
def plot_example(ax, zorder=0):
    ax.bar(tips_day["day"], tips_day["tip"], color="lightgray", zorder=zorder) # 요일별 평균데이터를 bar plot으로 만들기
    ax.set_title("tip (mean)", fontsize=16, pad=12) # 그래프 타이틀 지정옵션 

    # Values
    h_pad = 0.1 # 높이 여백설정 옵션 / 입력형태 : float
    for i in range(4): # 반복문 4번 실행
        fontweight = "normal" # 글자 굵기 노말 
        color = "k" # 색상지정 옵션
        if i == 3: # 조건문 i가 3이면
            fontweight = "bold" # 글자 굵기 굵게
            color = "darkred" # 색상 지정 옵션

        # bar위에 데이터를 글자로 넣기 
        ax.text(i, tips_day["tip"].loc[i] + h_pad, f"{tips_day['tip'].loc[i]:0.2f}", 
                horizontalalignment='center', fontsize=12, fontweight=fontweight, color=color)

    # Sunday
    ax.patches[3].set_facecolor("darkred") # set_facecolor()-> 그래프의 막대 색상지정 짙은 빨강
    ax.patches[3].set_edgecolor("black") # set_edgecolor()-> 그래프의 막대 테두리 색지정 검정

    # set_range
    ax.set_ylim(0, 4) # y축 범위
    return ax # ax값으로 리턴
```
<br>

## 예시자료 데이터 -> 조건에 맞게 평균출력
```python
tips = sns.load_dataset("tips") # 예시로 seaborn의 tips 데이터 불러오기
tips_day = tips.groupby("day").mean().reset_index() # groupby를 이용해 요일별 평균 데이터 생성
print(tips_day) # 요일별 평균 데이터 만든것을 출력ips = sns.load_dataset("tips") # 예시로 seaborn의 tips 데이터 불러오기
tips_day = tips.groupby("day").mean().reset_index() # groupby를 이용해 요일별 평균 데이터 생성
print(tips_day) # 요일별 평균 데이터 만든것을 출력
```

        day  total_bill       tip      size
    0  Thur   17.682742  2.771452  2.451613
    1   Fri   17.151579  2.734737  2.105263
    2   Sat   20.441379  2.993103  2.517241
    3   Sun   21.410000  3.255132  2.842105
    
<br>

## 시각화 호출 1
```python
fig, ax = plt.subplots(figsize=(10, 6)) # 그래프 호출 / figsize = 그래프 크기옵션
ax = plot_example(ax, zorder=2)  # 그래프내의 막대 시각화

##  spine 숨기기  
ax.spines["top"].set_visible(False) 
ax.spines["right"].set_visible(False)
ax.spines["left"].set_visible(False)
```



![](/image/image3/output_5_0.png)
    

<br>

## 시각화 호출 2
```python
fig, ax = plt.subplots() # 그래프 호출 
ax = plot_example(ax, zorder=2) # 그래프내의 막대 시각화

##  spine 숨기기  
ax.spines["top"].set_visible(False)
ax.spines["right"].set_visible(False)
ax.spines["left"].set_visible(False)

ax.yaxis.set_major_locator(MultipleLocator(1)) # major tick을 1 단위로 설정
ax.yaxis.set_major_formatter(formatter)  # major tick format 지정 (오류가 나면 matplotlib upgrade)
ax.yaxis.set_minor_locator(MultipleLocator(0.5)) # minor tick을 0.5 단위로 지정

ax.grid(axis="y", which="major", color="lightgray") # 그래프 표시선 넣기 -> major라인 실선
ax.grid(axis="y", which="minor", ls=":") # 그래프 표시선 넣기 -> minor라인 점선
# ax.grid(axis="y", which="both") -> major, minor 둘다  
```


    
![](/image/image3/output_6_0.png)

    


## 자료 출처 
* 참고블로그
    <https://jehyunlee.github.io/2020/08/27/Python-DS-28-mpl_spines_grids/>