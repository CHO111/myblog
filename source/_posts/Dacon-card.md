---
title: Dacon-card
date: 2021-06-16 19:40:21
tags: Machine learning , python
categories:
    - Project
    - Dacon
---
# 신용카드 사용자 연체 예측 AI 경진대회

![](https://github.com/CHO111/Project/blob/main/%EC%8B%A0%EC%9A%A9%EC%B9%B4%EB%93%9C%20%EC%82%AC%EC%9A%A9%EC%9E%90%20%EC%97%B0%EC%B2%B4%20%EC%98%88%EC%B8%A1%20AI%20%EA%B2%BD%EC%A7%84%EB%8C%80%ED%9A%8C_Dacon/image/dacon_project.png?raw=true)

## 콘테스트 개요

**1. 설명**

신용카드 사용자들의 개인 신상정보 데이터로 사용자의 신용카드 대금 연체 정도를 예측

**2. 도전목표**
* 현재 많은 금융업계는 인공지능(AI)를 활용한 금융 서비스를 구현하고자 합니다. 사용자의 대금 연체 정도를 예측할 수 있는 인공지능 알고리즘을 개발해 금융업계에 제안할 수 있는 인사이트를 발굴해주세요!
* 신용카드 사용자 데이터를 보고 사용자의 대금 연체 정도를 예측하는 알고리즘 개발 

**3. 평가**
* 심사 기준: Logloss
    * 1차 평가(Public Score): 테스트 데이터 중 랜덤 샘플 된 50%로 채점, 대회 기간 중 공개
    * 2차 평가(Private Score): 나머지 50 % 테스트 데이터로 채점, 대회 종료 직후 공개
    * 최종 순위는 선택된 파일 중에서 채점되므로, 참가자는 제출 창에서 자신이 최종적으로 채점 받고 싶은 파일 2개를 선택해야 함
* 2개의 선택 파일 중 높은 점수를 기준으로 최송 순위를 결정
    * 최종 파일 미선택시 처음으로 제출한 파일로 자동 선택됨
* 대회 직후 공개되는 Private Score 랭킹은 최종 순위가 아니며, 코드 검증 후 최종 수상자가 결정됨
* 대회 평가 규칙을 준수한 제출팀 중 Private Score를 기준으로 최종 순위를 결정

**4. 상품**
 * 1st ~ 10st : ₩ 100,000

**5. 참고**
　　※ 월간 데이콘은 데이콘 브론즈 이상의 티어를 갖고있는 분들만 수상이 가능합니다. 

**6. 기여**
 * xgboost 등 기법을 사용하여 정형 데이터 가공

**7. 결과** 
 * 714팀 중 404등 최종점수 - 0.70742

## 소스 코드
[code 보기](https://github.com/CHO111/Project/blob/main/%EC%8B%A0%EC%9A%A9%EC%B9%B4%EB%93%9C%20%EC%82%AC%EC%9A%A9%EC%9E%90%20%EC%97%B0%EC%B2%B4%20%EC%98%88%EC%B8%A1%20AI%20%EA%B2%BD%EC%A7%84%EB%8C%80%ED%9A%8C_Dacon/code/Simple_lightGBM.ipynb)

## 대회 발표 자료 
[pdf](https://github.com/CHO111/Project/blob/main/%EC%8B%A0%EC%9A%A9%EC%B9%B4%EB%93%9C%20%EC%82%AC%EC%9A%A9%EC%9E%90%20%EC%97%B0%EC%B2%B4%20%EC%98%88%EC%B8%A1%20AI%20%EA%B2%BD%EC%A7%84%EB%8C%80%ED%9A%8C_Dacon/file/%EC%8B%A0%EC%9A%A9%EC%B9%B4%EB%93%9C%20%EC%82%AC%EC%9A%A9%EC%9E%90%20%EC%97%B0%EC%B2%B4%20%EC%98%88%EC%B8%A1%20AI%20%EA%B2%BD%EC%A7%84%EB%8C%80%ED%9A%8C.pdf)