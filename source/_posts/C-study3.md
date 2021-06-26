---
title: C++_공부3
date: 2021-06-26 22:10:13
tags: Study
categories:
    - Study
    - C++
---
# C++ 기초부터 공부하기

## 반복문에 대해 알아보자.
반복문에는 for문과 while문이 있다.
for문은 -> 우리가 얼마만큼 반복을 시켜야 하는지 알떄 사용을한다.
while문은 -> 우리가 얼마만큼 반복을 시켜줘야 하는지 모를떄 / 어떻게 반복해야할지 조건만 알떄 사용한다.

```C++
int main()
{
    for (int i = 0;  i < 10; i++)
    {
        cout << "owl" << endl;
    }

    return 0; 
}
```

```C++
    int temp;
    int sum = 0;
    
    while (std::cin >> temp)
    {
        sum += temp;
    }
    std::cout << sum << std::endl;

    return 0; 
```
위 코드는 for문과 while문에대한 예시코드이다.
for문 코드는 owl을 10번 반복출력 시키는 코드이다 <br/>
while문 코드는 입력이 멈출떄까지 입력받은숫자를 더하는 코드이다 .
- 입력을 멈추는조건을 지정해주지 않았지만 ctrl + z 를 입력하면 입력을 멈춘다.

## 알아두어야할것들
- c++ 은 반복문안에서 변수를 만들수있다.
- cout의 특별한 기호 '\n'
- cin 의 특별한 기호 EOF (end of file) ctrl + z 키  
- 리눅스에서는 EOF (end of file)는 ctrl + D 키 


