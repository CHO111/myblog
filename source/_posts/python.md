---
title: python 기초문법
date: 2021-04-06 11:47:52
tags: python
category: Python
---

# 1. Hello World  출력
```python
print("Hello World");
```
    Hello, world!

# 2. 주석처리   
* 한줄주석처리 -> # 
* 여러줄 주석처리 -> 동일한 따옴표(""" or ''') 3개와 3개 사이에는 어떠한내용이 들어가도 주석처리가된다.

# 3. 사칙연산
```python
a = 5
b = 7
print('a + b = ', a+b); # 더하기
print('a - b = ', a-b); # 빼기
print('a * b = ', a*b); # 곱하기
print('a / b = ', a/b); # 나누기
print('a // b = ', a//b); # 몫
print('a % b = ', a%b); # 나머지
print('a ** b = ', a**b); # 거듭제곱
```
    a + b =  12
    a - b =  -2
    a * b =  35
    a / b =  0.7142857142857143
    a // b =  0
    a % b =  5
    a ** b =  78125


# 4. 문자열
```python
str1 = "Hello";
str2 = "World";
print('str1 + str2=', str1 + str2);

str = str1 + str2
print('str * 3 = ', str * 3);
```
    str1 + str2 =  Hello World 

    str * 3 =  Hello World Hello World Hello World 


# 5. Indexing
```python
str = "Hello World!";
print(str[6]);
```
    W


# 4. Slicing
```python
str = "Hello World!"
print(str[:])  # 인덱스 처음부터 끝까지
print(str[6:]) # 인덱스 6부터 끝까지 잘라서 출력
print(str[:6]) # 인덱스 0부터 5까지 잘라서 출력
print(str[2:8]) # 인덱스 2부터 7까지 잘라서 출력
print(str[0:9:2]) # 인덱스를 0부터 2씩 증가시키면서 8까지 출력
```
    Hello World!
    World!
    Hello 
    llo Wo
    HloWr


# 5. List
* 리스트
```python
a = [] # 빈 리스트
a_list = list() #list()함수로도 빈 리스트를 만들 수 있다.
b = [1] # 숫자도 요소가 될 수 있다.
c = ['str'] # 문자열도 요소가 될 수 있다
d = [1, 2, ['str']] # 리스트 안에 리스트를 요소로 넣을 수 있다.
```

        []
        []
        [1]
        ['str']
        [1, 2, ['str']]


```python
    a =    [1,    2,   3]
    # index [[0], [1], [2]]
    print(a[0]) # 첫번째 요소
    print(a[1]) # 두번째 요소
    print(a[2]) # 세번째 요소
    print(a[-1]) # 역순
```
    1
    2
    3
    3

```python
    a = [['str1','str2','str3']]
    print(a[0]) # 리스트 내의 리스트
    print(a[0][0]) # 리스트 내의 리스트의 첫번째 문자열
    print(a[0][0][3]) # 리스트 내의 리스트의 첫번째 문자열 'apple' 중 첫번째 인덱스
    print(a[0][1]) # 리스트 내의 리스트의 두번째 문자열
 ```

    ['str1', 'str2', 'str3']
    str1  
    1
    str2

* 리스트 값 수정
```python
a = [0,1,2]
a[1] = "b"

print(a)
```
       [0, 'b', 2]

* 리스트값 추가
```python
a = [1, 2, 3]
a.append(4)
print(a)

a.append([5,6])
print(a)
```
        [1, 2, 3, 4]

        [1, 2, 3, 4, [5, 6]]
```python
a = [0,1,2]

a.insert(1,7)
print(a)
```
        [0, 7, 1, 2]

* 리스트 값 삭제
```python
a =[1,2,1,2]

#리스트의 첫번째 1이 삭제
a.remove(1)
print(a)
```
        [2, 1, 2]
```python
a = [0,1,2,3,4,5]

# 1 삭제
del a[1]
print(a)

b = [0,1,2,3,4,5]
# 범위로 삭제
del b[1:3] #list는 항상 시작하는 index부터, 종료하는 n의 n-1까지의 범위를 잡아줍니다.
print(b)
```
        [0, 2, 3, 4, 5]

        [0, 3, 4, 5]

# 6. Tuple
```python
a = () # 비어있는 튜플생성
a1 = (0) # 값이 한개인경우 끝에 콤마(,)를 붙이지 않았을 때는 튜플 자료형이 아니다.
a2 = (0,) # 값이 한개인 경우 끝에 콤마(,)를 붙여줘야만 튜플형 자료형이다
a3 = 0,1,2 # 여러개의 값 일경우 괄호가 없어도 튜플 자료형이다
```

# 7. List 와 Tuple의 차이점
* 공통점
    * 1. list와 tuple모두 여러 데이터를 담을 수 있는 컨테이너형 변수이다.
    * 2. list와 tuple 모두 인덱스를 통해 특정 요소에 접근할 수 있다.
    * 3. list와 tuple 모두 iterable하다. 즉, for문에 넣고 돌릴 수 있다.
* 차이점
    * 1. list는 mutable(가변)하지만 tuple은 immutable(불변)하다.
    * 2. 따라서, list는 딕셔너리의 key값(해쉬값)으로 쓸 수 없지만, tuple은 가능하다.
    * 3. iteration을 도는 속도가 튜플이 더 빠르다.
    * 4. List는 내부의 값을 변경할수 있지만 Tuple은 내부의 값을 변경하거나 삭제를 할수없습니다.
    * 5. List생성은 대괄호[] Tuple생성은 소괄호()입니다.
    