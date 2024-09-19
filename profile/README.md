## HUB

### <span style="color:blue">MSA 기반 인공지능 알림 물류 서비스</span>


<br> <br/>
## 프로젝트 개요

### 프로젝트 주제

* MSA 기반 생성형 인공지능을 활용한 물류 시스템 서비스 구축



### 기획 배경

* 자동화된 물류 시스템 구축 필요

* 반복되는 형식의 보고서 작성 필요



### 프로젝트 목표

* 생성형 AI를 활용한 알림 및 보고서 작성을 통한 편의성 제공

* 유연한 상태 변경을 통한 배송 추적 편리화
* 지리 API 를 활용한 배송 경로 및 소요 시간 추적
* 확장 가능성을 고려한 아키텍처 설계



### Our Team

|                 박상훈                 |                 이범수                 |                조인희                |
| :------------------------------------: | :------------------------------------: | :----------------------------------: |
| [@shoon95](https://github.com/shoon95) | [@beomsu1](https://github.com/beomsu1) | [@InHees](https://github.com/InHeeS) |
|                   BE                   |                   BE                   |                  BE                  |

#### 🚚 [프로젝트 노션 바로가기](https://www.notion.so/HUB_AI_SERVICE-1052ebde9ffc8008a2a8c23f21cab914?pvs=4)


<br> <br/>
## 아키텍처 

![image](https://github.com/user-attachments/assets/b9644341-8ff8-47d9-8aec-2d5110184175)

<br> <br/>
## Application 구성

### User Application 

> USER

> ADMIN



### Hub Application

> HUB

> COMPANY

>  PRODUCT

* 허브 정보를 활용하여 재귀적으로 경로를 생성합니



### Order Application

> ORDER

> DELIVERY
>
> 

### AI-Slack Applciation

> AI

> SLACK


<br> <br/>
## 프로젝트 기능

### Slack 인증을 통한 회원 가입

> * 회원 가입 후 slack 메세지를 활용하여 인증 후 계정 활성화가 가능합니다.


<br> <br/>
## 적용 기술

### ㅁ Redis

> slack을  인증 시 인증 코드를 Redis에 저장하여 TimeToLive를 설정했으며, DB에 접근하지 않아도 되도록 했습니다.


<br> <br/>
## 트러블 슈팅

* 확장성을 고려한 권한 별 유저 회원 가입 문제


<br> <br/>
## ERD




<br> <br/>
## 기술 스택

- ![Java](https://img.shields.io/badge/Java17-%23ED8B00.svg?style=square&logo=openjdk&logoColor=white) <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=square&logo=springboot&logoColor=white"> <img src="https://img.shields.io/badge/Spring Security-6DB33F?style=square&logo=Spring Security&logoColor=white"> ![Spring Data JPA](https://img.shields.io/badge/Spring%20Data%20JPA-6DB33F?style=square&logo=Spring&logoColor=white) ![Spring Gateway](https://img.shields.io/badge/Spring%20Gateway-6DB33F?style=square&logo=Spring&logoColor=white) <br>
![Spring Cloud](https://img.shields.io/badge/Spring%20Cloud-6DB33F?style=square&logo=Spring&logoColor=white) ![Eureka](https://img.shields.io/badge/Eureka-6DB33F?style=square&logo=Spring&logoColor=white) ![Resilience4j](https://img.shields.io/badge/Resilience4j-6DB33F?style=square&logo=Spring&logoColor=white) ![JWT](https://img.shields.io/badge/JWT-black?style=square&logo=JSON%20web%20tokens) ![Gradle](https://img.shields.io/badge/Gradle-02303A.svg?style=square&logo=Gradle&logoColor=white)
- ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1.svg?style=square&logo=PostgreSQL&logoColor=white)
- <img src="https://img.shields.io/badge/Docker-%230db7ed.svg?style=square&logo=docker&logoColor=white">
- ![GitHub](https://img.shields.io/badge/Github-%23121011.svg?style=square&logo=github&logoColor=white) ![Slack](https://img.shields.io/badge/Slack-4A154B?style=square&logo=slack&logoColor=white) ![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ%20IDEA-000000.svg?style=square&logo=intellij-idea&logoColor=white) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=square&logo=postman&logoColor=white) ![Notion](https://img.shields.io/badge/Notion-%23000000.svg?style=square&logo=notion&logoColor=white)

* ![Google Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?style=square&logo=Google%20Gemini&logoColor=white)

* ![Zipkin](https://img.shields.io/badge/Zipkin-black?style=square&logo=Zipkin&logoColor=white) ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=square&logo=Prometheus&logoColor=white) ![Grafana](https://img.shields.io/badge/Grafana-F46800?style=square&logo=Grafana&logoColor=white)

