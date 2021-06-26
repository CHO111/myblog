---
title: C++_공부2
date: 2021-06-26 21:55:35
tags: Study
categories:
    - Study
    - C++
---
# C++ 기초부터 공부하기

## 콘솔 입출력
c++_공부1 에 이어서 입출력에대해 자세히 알아보자.

```C++
int main()
{
    int a;
    int b;
    std::cin >> a;
    std::cin >> b;
    std::cout << a << " " << b << std::endl;

    return 0; 
}
```
위코드는  숫자 두개를 입력받아 출력시키는 코드이다 
여기서 cin의 단점이 있는대 
cin은 중간에 공백이 들어가면 인식을멈추고 다음 cin 한대 일을 맡겨버리는 단점이 있다 .

![](https://user-images.githubusercontent.com/54093963/123513886-b1396a80-d6ca-11eb-867f-11e524104cdb.PNG)
위 사진이 정상적으로 입력햇을때 나오는결과이다.
![](https://user-images.githubusercontent.com/54093963/123513888-b26a9780-d6ca-11eb-8cae-b53978d0d202.PNG)
위 사진은 입력 받은 숫자뒤에 공백을 넣고 한번더 입력을하면 바로 결과가 나와버리는 cin의 단점을 보여주는 결과이다.

## 알아두어야할것들
- std::endl 이친구는 개행을 시켜주는 함수
- '\n'(개행문자)
- cin 은 공백문자나 개행문자같은것을 무시한다
- getline()을쓰면 공백문자도 다 읽는다.
- enter을 누르면 컴파일러한대 암묵적으로 개행을 시켜라 라고 지시

