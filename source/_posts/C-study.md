---
title: C++_공부
date: 2021-06-26 21:33:37
tags: Study
categories:
    - Study
    - C++
---
# C++ 기초부터 공부하기
메인 함수는 뭘까 ?
- 메인함수는 운영체제가 프로그램이 시작될떄 호출하는 함수다.

## 콘솔 입출력
입력은 cin 출력은 cout이다 . 입출력에 대하여 알아보자.

```C++
int main()
{
    int OWL{ 10 };
    double Num{ 9.8 };
    int Myage;

    //출력은 두종류로 쓸수있다 '\n' 로 마무리하거나 endl로 마무리하는법이 있다.
    std::cout << "hello world" << '\n'; 
    std::cout << "hello world" << std::endl; // cout은 함수가 아니라 객체다
    
    //c++를 만든 사람들이 cout을 엄청 똑똑하게 만들었다 .
    std::cout << OWL << std::endl; 
    std::cout << Num << std::endl;

    printf("hello world\n"); // frintf는 함수다 
    printf("%d\n", OWL); // 오래되서 멍청하다
     //  <<  이 연산자는 출력 연산자다.
     
    return 0; // main 함수에 있는 리턴 0는 프로그램이 꺼질때 운영체제한대 얘가 끝낫다라는것을 말한다.
}
```
위 코드에 c++의 cout과 c의 printf에 대해 비교주석을 써놓았는대
cout은 자료형을 알아서 읽어서 출력하지만 printf은 서식(자료형)에대해 입력을 해주어야 출력이 된다.


