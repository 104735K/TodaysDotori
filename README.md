## 🐿 💼 출퇴근 생활 정보 시스템 (TodaysDotori)

<img width="778" alt="Image" src="https://github.com/user-attachments/assets/4ff88c3e-d261-43bc-bf19-11b6ce18c9d9" />

## 💻 PROJECT INTRODUCTION
- 목적
  - 출퇴근에 필요한 날씨 정보, 버스 및 지하철 위치, 주변 따릉이 정류소와 따릉이 갯수 등을한 페이지에 제공하여 사용자에게 편리한 출퇴근 정보 제공
  - 공공데이터 API를 사용하여 API 활용 능력 극대화, 데이터 기반의 인사이트 도출

- 기능
  -  현재 위치 기반 날씨 데이터 출력
  - 지정한 버스 정류장의 버스의 실시간 위치 제공
  - 자주 이용하는 지하철의 실시간 도착 정보 제공
  - 사용자의 현재 위치에 따른 따릉이 정류소 및 갯수 정보 제공

## 🗓️ DEVELOPMENT PERIOD
2024.12 - 2024.12

## 👩🏻‍💻🧑🏻‍💻TEAM
|이름|역할|
|:------:|---------------|
|강성현|화면설계, 기상청API를 활용한 실시간 날씨 정보 및 최근 3일간의 과거/예측 날씨 조회|
|강하나|실시간 지하철 위치 정보 API 호출|
|김찬|실시간 버스 위치 정보 API호출, DB 프로시저 담당|


## ⚙️ DEVELOPMENT ENVIRONMENT
- Programming Language : Java 17
- Framework : Spring Boot
- Database : MongoDB
- Front : HTML/CSS, JavaScript, Bootstrap
- Tooling/ DevOps : Intellij IDEA, GitHub, Docker, Postman ..
- Environment : MacOS
- Etc : Figma, Slack

## 💡 FEATURE
> <h3>강성현 주요 기능</h3>
### ☀️ 실시간 날씨 정보 제공
- 세션에 저장된 사용자의 실시간 위치 정보를 조회
- 사용자의 3차 주소를 받아 MongoDB에서 nx, ny 좌표 값 조회 및 출력
- 공공데이터 API를 활용하여 실시간 날씨 데이터(초단기실황, 초단기예보) 요청
- API 응답 데이터를 파싱, UI 가공 및 표시

### 👀 화면 설계
- 하나의 페이지에 모든 정보를 한 눈에 볼 수 있도록 구현

## 📂 PROJECT STRUCTURE
```

└── src
    ├── main
    │   ├── generated
    │   ├── java
    │   │   └── com
    │   │       └── TodaysDotori
    │   │           ├── HomeController.java
    │   │           ├── TodaysDotoriApplication.java
    │   │           ├── config
    │   │           │   └── Config.java
    │   │           ├── controller
    │   │           │   ├── LocationController.java
    │   │           │   ├── SubwayStationController.java
    │   │           │   └── WeatherController.java
    │   │           ├── domain
    │   │           │   ├── SubwayStation.java
    │   │           │   └── Weather.java
    │   │           ├── repository
    │   │           │   ├── SubwayStationRepository.java
    │   │           │   └── WeatherRepository.java
    │   │           └── service
    │   │               ├── LocationService.java
    │   │               ├── LocationServiceImpl.java
    │   │               ├── SubwayStationService.java
    │   │               ├── SubwayStationServiceImpl.java
    │   │               ├── WeatherService.java
    │   │               └── WeatherServiceImpl.java
    │   ├── resources
    │   │   ├── application.properties
    │   │   ├── static
    │   │   │   ├── css
    │   │   │   │   ├── index.css
    │   │   │   │   └── location.css
    │   │   │   ├── image
    │   │   │   │   └── locationPin.svg
    │   │   │   └── js
    │   │   │       ├── bus.js
    │   │   │       ├── common
    │   │   │       │   └── jquery-3.7.1.js
    │   │   │       ├── location.js
    │   │   │       ├── publicBike.js
    │   │   │       ├── subway.js
    │   │   │       └── weather.js
    │   │   └── templates
    │   └── webapp
    │       └── WEB-INF
    │           └── views
    │               ├── bus.jsp
    │               ├── index.jsp
    │               ├── location.jsp
    │               ├── publicBike.jsp
    │               ├── subway.jsp
    │               └── weather.jsp
    └── test
        └── java
            └── com
                └── TodaysDotori
                    └── TodaysDotoriApplicationTests.java

```
