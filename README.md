# FinalAconProject

## 1. 주제

사진으로 어떤 알약인지 판별

## 2. 주제 선정 배경

집에 약국에서 사서 한 두 알을 남긴 채 방치되어져 있는 알약들이 많이 있다.
이 알약들은 얼마 남지 않았고 나중에 보면 무슨 약인지 기억할 수 있다는 확신으로 약만 남긴채 곽을 버리곤 한다.
하지만 진짜 필요한 순간에 찾아보면 무슨 알약인지 복용법은 무엇인지 주의사항 또한 기억하지 못한다.
그럴 때, 알약을 사진으로 찍어서 판별해주는 애플리케이션이 있으면 어떨까? 하는 궁금증에서 이 주제를 고안했다.

## 3. 분석 계획
### 3.1. 데이터 수집 및 관리

드럭인포, 약학 정보원 과 같은 사이트에서 약의 사진과 함께, 약의 정보를 웹 크롤링<br>
mySQL을 활용하여 DB에 저장한다.<br>
DB에 저장할 정보 : 약의 이름, 사진, 유통기한, 성분, 주의사항, 위험도 등등

### 3.2. 전처리

약명이 다르게 표기되었을 지라도, 영어를 한글로, 한글을 영어로 표기하는 등의 중복 표기가 있을 수 있음.<br>
약의 종류와 양이 너무 많으므로, 특정한 기준을 정해서 종류는 줄이도록 함.<br>
크롤링해온 정보들의 공통점을 파악해서 정리해야 함. <br>
약 사진의 다양성이 부족함, 이것을 늘릴 방법이 필요.

### 3.3. 분석 기법

이미지 분석을 진행 해야 함.<br>
딥러닝을 기반으로 진행(CNN, AlexNet 등)

## 4. 애플리케이션 구상

궁금한 알약을 검색하기 위한 버튼<br>
버튼을 누르고 들어가서 자신이 궁금한 알약의 윗면과, 아랫면을 사진 찍게 함<br>
알약의 이름이 무엇이고, 복용법은 무엇인지, 주의사항은 무엇이고, 어떤 약과 함께 먹으면 안되는 지 까지 보여주면 완성!
