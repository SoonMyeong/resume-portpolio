# e-Navigation 서비스 중개 서버 고도화 1차 연구 과제
## 아키텍처
![image](https://github.com/SoonMyeong/resume-portpolio/assets/31875043/a2e95305-964a-483f-9e93-bab8a9c89e13)


### 투입 인원
- PM 1명, 개발자 2명
### 내용
- API Gateway, Eureka 도입 및 도메인 분리 설계
  - 서버 부하 분산 용이
    - 현재 운영센터의 경우, 선박과 서비스 모두 해당 서버로 요청 및 응답을 보내고 있는 상태
  - scale out 에 유연
    - 유레카를 통해 로드밸런싱이 가능하므로 분리 된 각 서비스들을 여러 개로 구성할 수 있음
  - 협업 개발 시 전체 시스템 이해도 감소
    - 개발하는 부분 서비스만 먼저 파악해도 개발 가능
    - 새로 투입된 개발자 1명과 의사 소통 하기 원활
- 2차, 3차 연구 과제에 신규 비즈니스 내용이 생길 경우 확장 용이

### 세부 내용
- 기존 Netty 만 사용 → Spring IoC/DI 기능 사용하기 위해 Spring Webflux 사용
- RabbitMQ Connection Pool 만 사용 → Channel Pool 사용
  - 물리 커넥션 99% 감소 (300 - 500 개 -> 2~3개)
- API 추적을 위한 Slueth & zipkin 도입
