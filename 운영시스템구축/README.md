# e-Navigation 연구과제 운영 시스템 구축
## 아키텍처
![image](https://github.com/SoonMyeong/resume-portpolio/assets/31875043/636d1fbd-23d5-4fc0-8812-5880bcd44925)


### 투입 인원
- PM 1명, 개발자 1명
### 내용
- 모바일 앱에서 인터넷 망으로 e-Navigation 서비스 이용
- 선박에 설치한 장비로 연결할 경우 LTE 망으로 접근
- 기존 로컬 캐시로만 관리되던 선박의 정보를 DB 와 Redis 에 적재 하게 변경
  - 사용자가 자신의 정보를 입력 해 선박 ID 를 직접 등록할 수 있음(단, 전용 인증서를 먼저 발급 받아야 함)
-       
