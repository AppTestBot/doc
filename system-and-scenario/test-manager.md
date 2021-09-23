---
description: 로봇의 흐름과 전체 시스템을 제어하는 모듈에 대해서 설명합니다.
---

# Robot Manager

### 1.1. 로봇 매니저 역할 

1. 로봇 동작의 흐름 및 **전체 시스템을 제어**하는 모듈  
2. 각 서빙 모듈에게 요청을 보내 **하나로 동작**하는 역할 

### 1.2. 로봇 매니저 시퀀스 다이어그램 



![&#xB85C;&#xBD07; &#xB9E4;&#xB2C8;&#xC800;&#xC758; &#xB3D9;&#xC791; &#xC2DC;&#xD000;&#xC2A4; &#xB2E4;&#xC774;&#xC544;&#xADF8;&#xB7A8;](../.gitbook/assets/image%20%2812%29.png)

1. **Robot Manager**는 내용 기록을 위해 **녹화시작 요청**을 **Streaming/Recorder 서빙 모듈**에게 전달 
2. **Robot Manager**는 실험 시작시간을 **Robot Controller에 보내** 실험시작시간을 저장함
3. **Robot Manager**가 **Packet Collector**에게 **패킷 수집** 요청 
4. **Robot Manager**는 **Robot Controller** 에게 **앱 시작** 요청 전송
5. **Robot Manager**는 **Robot Controlle**r에게 실험 횟수만큼 **터치 명령**을 전송
6. **Robot Controller**는 **Object Detection**에게 클릭 **좌표를 요청/응답** 
7. **Robot Manager**는 실험후 **Performance Analyzer**에게 **성능 분석기 실행**하도록 요청 

