# PAAS-TA-PORTAL-CONFIG-SERVER


## Config Server
config server 를 간단히 설명하면, 다른 서버들의 설정을 제공하는 서비스

예를 들어, 어떤 API Server 가 있다면, 설정에 자신의 서비스 이름과 config server 주소만 적어주면 됩니다. 그리고 config server 에 해당 API Server에 사용될 port 정보나 여러가지 설정들이 들어가게 됩니다. 보통 시작 Port는 설정 파일이나, 코드에 입력돼있는 경우도 흔한데, 이럴 경우 쉽게 설정을 변경하기가 어렵습니다. 즉, config server는 설정을 바꿀 때 Git 에서 받아와서 각각의 서비스를 실행하게 하는 것이 핵심. 그래서 Eureka 서버, API Gateway 등 모든 서비스가 config server에 접근하여 해당 설정을 가져가게 됩니다.

- 환경변수를 제공해주는 REST API 서버(필수)와  환경변수를 받는 클라이언트로 구성(옵션)
- JSON 형식으로 제공(어떤 서버에서도 사용 가능)
- 환경변수 관리(GIT, SVN, 로컬 file 등 이용)
- 환경변수에 대한 암/복호화 기능 내장
- 다양한 Application, Profile, Version 형태를 지원
- 코드와 설정의 분리


## 유의사항

개발 정보
- java 1.8 버전
- SpringCloud Edgware.RELEASE 
- TomcatEmded 8.5.14
- Gradle 4.4.1
- Spring-boot 1.5.9
- Redis 1.3.1


