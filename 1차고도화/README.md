# e-Navigation 서비스 라우터 고도화 1차 연구 과제
## 아키텍처
![image](https://github.com/SoonMyeong/resume-portpolio/assets/31875043/16d8e374-4aea-48de-9e8c-1391a6788d1d)



### 투입 인원
- PM 1명, 개발자 2명

### 배경
- 서비스 라우터 고도화를 통해 좀 더 많은 기능을 제공하고 분산 서비스를 운영하기 위함
### 내용
- API Gateway, Eureka 도입 및 도메인 분리 설계
- Channel Pool 사용 -> 물리 커넥션 99% 감소 (300 - 500 개 → 2~3개)
  - RabbitMQ Connection Pool 사용 → Channel Pool 사용 
- Slueth & zipkin 도입
  - API 추적을 pinpoint 처럼 한눈에 볼 수 있음   
- scale out 에 유연
  - 유레카를 통해 로드밸런싱이 가능하므로 분리 된 각 서비스들을 여러 개로 구성
- 협업 개발 시 전체 시스템 이해도 감소
  - 개발하는 부분 서비스만 먼저 파악해도 개발 가능
  - 인력이 새로 투입될 경우, 전체 서비스에 대한 이해 없이도 개발 가능 및 의사 소통 원활
- 2차, 3차 연구 과제에 신규 비즈니스 내용이 생길 경우 확장 용이
  - 기존 메시지 변환 서비스 통합 구성 시 용이
