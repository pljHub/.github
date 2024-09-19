## HUB

### <span style="color:blue">MSA 기반 인공지능 알림 물류 서비스</span>


<br> <br/>
## 📘 프로젝트 개요

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
## 🌐 아키텍처 

![image](https://github.com/user-attachments/assets/b9644341-8ff8-47d9-8aec-2d5110184175)

<br> <br/>
## 🛠 Application 구성

### User Application 

> USER

> ADMIN



### Hub Application

> HUB

> COMPANY

>  PRODUCT

* 허브 정보를 활용하여 재귀적으로 경로를 생성합니다.



### Order Application

> ORDER

> DELIVERY
>
> 

### AI-Slack Applciation

> AI

> SLACK


<br> <br/>
## 🏅 프로젝트 기능

### [Slack 인증을 통한 회원 가입](https://horse-giver-fbd.notion.site/Slack-fff2ebde9ffc810c8dd2f72fa8aaa571?pvs=4)

> * 회원 가입 후 slack 메세지를 활용하여 인증 후 계정 활성화가 가능합니다.

### [검색 기능](https://horse-giver-fbd.notion.site/Slack-fff2ebde9ffc810c8dd2f72fa8aaa571?pvs=4)

> * QueryDSL 과 Pagenation을 활용하여 동적 쿼리작성이 가능하도록 구현하였습니다.

### [FeignClient를 활용한 MSA 환경에서 트랜잭션 전파와 장애 대응](https://horse-giver-fbd.notion.site/FeignClient-MSA-fff2ebde9ffc8184858df45208b4b834?pvs=4)

> * FeignClient를 활용하여 MSA 환경에서의 통신을 구현하였습니다. 


### [CustomArgumentResolver를 활용한 공통 기능 개발](https://horse-giver-fbd.notion.site/CustomArgumentResolver-3d279a7928fd48e9990f021278b2a31a?pvs=4)

> * PageableArgumentResolver를 커스텀하며 파라미터의 중복을 줄이며 Login 어노테이션을 만들어 헤더로부터 전달받은 값들을 편리하게 쓰도록 변형하였습니다. 

### [GoogleMaps API를 이용한 위치 정보](https://horse-giver-fbd.notion.site/GoogleMaps-API-fff2ebde9ffc81929c48c3d22e07e65a?pvs=4)

> * Google Maps API를 활용하여 각 주소의 위치 좌표를 추출하며, 실시간 도로 정보를 기반으로 이동 시간을 반환합니다.

<br> <br/>
## 📃 적용 기술

### Redis

> slack을  인증 시 인증 코드를 Redis에 저장하여 TimeToLive를 설정했으며, DB에 접근하지 않아도 되도록 했습니다.

### QueryDSL

> 정렬, 검색어 등에 따른 동적 쿼리 작성을 위하여 QueryDSL 도입하여 활용했습니다.

### FeignClient

> MSA 환경에서 FeignClient를 사용하는 이유는 서비스 간 통신을 간편하게 관리하고 REST API 호출을 추상화하여 개발 생산성을 높이기 위해 활용했습니다. 


### Zipkin

> 분산 트레이싱을 통해 MSA 환경에서 각 서비스의 요청 흐름을 추적하고 성능 문제를 진단하기 위해 사용됩니다.


### Grafana 

> MSA 환경에서 수집된 메트릭 데이터를 시각화하여 시스템 모니터링과 성능 분석을 직관적으로 할 수 있게 사용됩니다.

### Sheduler를 통한 보고서 작성

> 배송 담당자는 매일 아침 6시에 당일 날씨와 배송에 대한 요약정보를 슬랙으로 전달받습니다. 


<br> <br/>
## 🚨 트러블 슈팅

* ### [확장성을 고려한 권한 별 유저 회원 가입 문제](https://horse-giver-fbd.notion.site/fff2ebde9ffc812ab774f726df939dfc)

* ### [= 연산자 사용으로 재귀 쿼리 결과가 제한됨](https://horse-giver-fbd.notion.site/fff2ebde9ffc81b3b065c6187ebb4acf)

* ### [주문 생성 중 상품의 재고 부족 문제로 인한 로직 롤백 처리](https://horse-giver-fbd.notion.site/fff2ebde9ffc813fa5e6e71e8980c6d8)


<br> <br/>
## ✏ ERD
![image](https://file.notion.so/f/f/c7724213-30b1-4b2e-a8db-0c2df548c441/78de94ea-165a-4103-b0bb-0c4211447831/hub.png?table=block&id=1052ebde-9ffc-8066-9219-f9da1a440769&spaceId=c7724213-30b1-4b2e-a8db-0c2df548c441&expirationTimestamp=1726804800000&signature=TlzJ2RjrF8MV6_lqYyeCSFtMqj0ubsnKU4f6PwS8qJQ&downloadName=hub.png)




<br> <br/>
## 💡 기술 스택

- ![Java](https://img.shields.io/badge/Java17-%23ED8B00.svg?style=square&logo=openjdk&logoColor=white) <img src="https://img.shields.io/badge/Spring%20Boot-6DB33F?style=square&logo=springboot&logoColor=white"> <img src="https://img.shields.io/badge/Spring Security-6DB33F?style=square&logo=Spring Security&logoColor=white"> ![Spring Data JPA](https://img.shields.io/badge/Spring%20Data%20JPA-6DB33F?style=square&logo=Spring&logoColor=white) ![Spring Gateway](https://img.shields.io/badge/Spring%20Gateway-6DB33F?style=square&logo=Spring&logoColor=white) <br>
![Spring Cloud](https://img.shields.io/badge/Spring%20Cloud-6DB33F?style=square&logo=Spring&logoColor=white) ![Eureka](https://img.shields.io/badge/Eureka-6DB33F?style=square&logo=Spring&logoColor=white) ![Resilience4j](https://img.shields.io/badge/Resilience4j-6DB33F?style=square&logo=Spring&logoColor=white) ![JWT](https://img.shields.io/badge/JWT-black?style=square&logo=JSON%20web%20tokens) ![Gradle](https://img.shields.io/badge/Gradle-02303A.svg?style=square&logo=Gradle&logoColor=white)
- ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1.svg?style=square&logo=PostgreSQL&logoColor=white)
- <img src="https://img.shields.io/badge/Docker-%230db7ed.svg?style=square&logo=docker&logoColor=white">
- ![GitHub](https://img.shields.io/badge/Github-%23121011.svg?style=square&logo=github&logoColor=white) ![Slack](https://img.shields.io/badge/Slack-4A154B?style=square&logo=slack&logoColor=white) ![IntelliJ IDEA](https://img.shields.io/badge/IntelliJ%20IDEA-000000.svg?style=square&logo=intellij-idea&logoColor=white) ![Postman](https://img.shields.io/badge/Postman-FF6C37?style=square&logo=postman&logoColor=white) ![Notion](https://img.shields.io/badge/Notion-%23000000.svg?style=square&logo=notion&logoColor=white)

* ![Google Gemini](https://img.shields.io/badge/Google%20Gemini-8E75B2?style=square&logo=Google%20Gemini&logoColor=white)

* ![Zipkin](https://img.shields.io/badge/Zipkin-black?style=square&logo=Zipkin&logoColor=white) ![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=square&logo=Prometheus&logoColor=white) ![Grafana](https://img.shields.io/badge/Grafana-F46800?style=square&logo=Grafana&logoColor=white)

