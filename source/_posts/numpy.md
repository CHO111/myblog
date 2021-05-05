---
title: Numpy 정리
date: 2021-04-06 15:54:47
tags: python
---

# 1. Numpy 기본함수
* arange
```python
arrange_array = np.arange(5)
arrange_array
```
        array([0, 1, 2, 3, 4])
        # array [0, 1, 2, 3, 4]의 형태로 반환
```python
arrange_array2 = np.arange(1, 9, 3)
arrange_array2
```
        array([1, 4, 7])
        # 1부터 시작 9까지 3간격으로 array[1, 4, 7] 형태로 반환 

<br>

* zoroes
```python
zeros_array = np.zeros((3,2))
print(zeros_array)
print("Data Type is:", zeros_array.dtype)
print("Data Shape is:", zeros_array.shape)
```
        [[0. 0.]
         [0. 0.]
         [0. 0.]]
        Data Type is: float64
        Data Shape is: (3, 2)

<br>

* ones
```python
ones_array = np.ones((3,4), dtype='int32')
print(ones_array)
print("Data Type is:", ones_array.dtype)
print("Data Shape is:", ones_array.shape)
```
        [[1 1 1 1]
         [1 1 1 1]
         [1 1 1 1]]
        Data Type is: int32
        Data Shape is: (3, 4)

<br>

* reshape
```python
after_reshape = ones_array.reshape(6,2)
print(after_reshape)
print("Data Shape is:", after_reshape.shape)
```
        [[1 1]
         [1 1]
         [1 1]
         [1 1]
         [1 1]
         [1 1]]
        Data Shape is: (6, 2)