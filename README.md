# 1조 무선네트워크 프로젝트
**팀원 : 김민규, 한용준, 서예령, 신건호, 이정우, 김건우**

--- 
### 프로젝트 아이디어 의견제시
> 23.10.31 ~ 23.11.06

1. **CCTV (*카메라, ~~적외선 센서~~*)**
   1. ~~보안용 CCTV: 사람의 움직임 감지시 동영상 녹화 또는 실시간 확인 시스템~~
   2. ~~기능 추가 고려사항: 실내용 CCTV가 아닌 다방면의 방향성 모색~~
   3. 공사장같은 장소의 모니터링 시스템, AI모델을 통한 작업자들의 사고 감지시 후 감독관에게 전송 및 신고시스템
      >참고자료   
      > https://eehoeskrap.tistory.com/348   
      > https://hackmd.io/@NrN0buuTTp6lMAQ5lPMhNw/ry5D6WFnc   
      >관련논문   
      > https://scienceon.kisti.re.kr/commons/util/originalView.do?cn=JAKO201761242144589&oCn=JAKO201761242144589&dbt=JAKO&journal=NJOU00567471<br>
      >cctv 모션감지에 대한 참고자료<br>
      >https://return-value.tistory.com/106<br>
      >https://scribblinganything.tistory.com/544
      
      
~~2. 글자 인식 카메라 (*카메라*)~~
   1. 글자 번역 제공 카메라
   2. 사진 및 책, 문서 스캐너
~~3. 시각장애인 보조 지팡이 (*GPS, RFID, UWB모듈 중 한가지 사용*)~~
   1. 횡단보도, 차도 등에 도착시 시각장애인에게 도로의 정보를 제공
   2. 기능 추가 고려사항: 도착시 시각장애인 신호 알림 받을 수 있는 방향 모색
~~4. 차량 전화번호 태그기기 (*NFC, RFID 등 태그관련 모듈 사용*)~~
   1. 핸드폰으로 태그시 시스템을 통한 차주인에 대한 정보제공(안심번호, 문자전송, 로그기록)

---
### 프로젝트 아이디어 수립 및 기능제시
1. 산업현장 안전관리 모니터링 카메라
2. 목적
   - 산업현장 같은 곳에서 이런 cctv 장치의 배치가 적게 되어 사고가 발생해도 다음날 발견되는 경우가 많아 그런 부분을 감소시키기 위해서이다.
   - <img width="1103" alt="스크린샷 2023-11-14 오전 10 05 42" src="https://github.com/inhatc-wn/inhatc/assets/113413158/c2fec221-dd9a-4221-a858-8dc4ff407a4b">
   - <img width="767" alt="스크린샷 2023-11-14 오전 10 07 56" src="https://github.com/inhatc-wn/inhatc/assets/113413158/2d0e5109-c4d5-4184-b695-3008c8674145">
   - <img width="1103" alt="스크린샷 2023-11-14 오전 10 05 42" src="https://github.com/inhatc-wn/inhatc/assets/113413158/7eb2a5dd-bf55-457a-bbc9-7d909cb7756d">
   
3. 기능 : 쓰러짐 감지, 특정 행동 감지, 실시간 모니터링 및 로그 누적
   - 쓰러짐 감지 : 근로자가 쓰러짐을 감지하면, 관리자에게 알림을 전송
   - 특정 행동 감지 : 근로자의 특정행동을 감지하여 그에 맞는 알림을 전송한다. (사고 신고 모션인식 등)
4. 구조
   1. 라즈베리파이 + 카메라
   2. 실시간 모니터링 웹페이지 및 앱
   3. API서버(AWS) (알림전송, 모델적용, 기타 기능구현 서버)<br>

