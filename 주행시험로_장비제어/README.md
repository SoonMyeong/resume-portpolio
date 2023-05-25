# 한국타이어 주행 시험로 장비 제어 프로그램 개발
## 아키텍처
![image](https://github.com/SoonMyeong/resume-portpolio/assets/31875043/229f4e28-3bb3-4e7d-814d-994647582eae)

## 내용
- 차단기, 전광판 제어를 위해 Netty framework 를 이용, 예약 웹에서 요청하는 데이터를 처리하기 위한 SpringBoot 이용
  - 제공된 RFID 카드를 소지 하고 있는 운전자는 허가 된 시간에 주행시험로를 이용할 수 있음
    - RFID 리더기 서버 통신 : TCP 통신
  - 전광판에 트랙 사용 현황을 보여줌
    - 전광판 통신 : TCP 통신 
  - 시험 주행로 예약 웹에서 관리자의 경우 주행시험로를 원격으로 제어할 수 있음
    - 예약 웹서비스 통신 : HTTP 통신 

- 한국타이어 측의 예약 정보를 가져오기 위해 Spring Batch 이용
