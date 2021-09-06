---
description: 로봇의 흐름과 전체 시스템을 제어하는 모듈에 대해서 설명합니다.
---

# Robot Manager

### 1.1. 로봇 매니저 역할 

1. 로봇 동작의 흐름 및 전체 시스템을 제어하는 모듈  
   1. 각 모듈의 동작 sync를 맞춰주어야함
   2. 시작 명령/ 중지 명령을 같이해야함
2. 각 서빙 모듈에게 요청을 보내 하나로 동작하는 역할 
3. 필요에 따라 subprocess를 통해 모듈과 통신\(packet 수집기\)

### 1.2. 로봇 매니저 시퀀스 다이어그램 



![&#xB85C;&#xBD07; &#xB9E4;&#xB2C8;&#xC800;&#xC758; &#xB3D9;&#xC791; &#xC2DC;&#xD000;&#xC2A4; &#xB2E4;&#xC774;&#xC544;&#xADF8;&#xB7A8;](../.gitbook/assets/image%20%2811%29.png)

1. Robot Manager는 내용 기록을 위해 녹화시작 요청을 Streaming/Recorder 서빙 모듈에게 녹화하는 요청을 전
2. Streaming/Recorder 응답을 보냄과동시에 녹화를 시작
3. Robot Manager는 실험 시작시간\(성능분석에 필요\)을 로봇 제어기에 보내 실험시작시간을 저장함
4. subprocess를 통해 패킷 수집기에 패킷을 수집하라는 명령을 보내고, 패킷 수집기는 공유기의 tcpdump를 통해 패킷수집을 시작하고, subproess의 PID를 로봇 매니저에게 전송하여 프로세스의 시작을 알
5. Robot Manager는 Robot Controller 에게 앱을 시작하라는 요청을 전송
6. 앱이 실행되면 Robot Controller는 200 OK를 전송 
7. Robot Robot Controller는 로

