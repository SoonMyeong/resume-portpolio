# e-Navigation 메시지 변환 서비스 과제
## 아키텍처
![image](https://github.com/SoonMyeong/resume-portpolio/assets/31875043/b5e1890c-510d-460d-9e7d-bb62e75792c5)

### 투입 인원
- PM 1명, 개발자 2명
### 내용
- 역할
  - 서비스 라우터에서 HTTP 통신으로 전달 된 XML 데이터를 육상 서비스의 Topic 내용에 맞게 메시지를 변환 하여 DDS 통신으로 전달 해 주는 역할
  - 반대로 육상 서비스에서 DDS 통신으로 Topic 을 전달 하면 해당 내용을 XML 데이터 혹은 JSON 데이터로 변환 하여 다시 서비스 라우터로 전달 하는 역할
- RabbitMQ 를 중간에 둬서 내부 gateway 와의 통신 간 메시지 유실을 방지할 수 있음
- 분기 마다 연구 센터에 방문하여 개발 내용 시연
