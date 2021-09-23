---
description: >-
  Streaming, Recording, Click Predictor 세가지 기능을 수행하기 만들어진 Image Analzyer에 대하여
  설명합니다.
---

# Image Analyzer

![&#xCE74;&#xBA54;&#xB77C; &#xC2A4;&#xD2B8;&#xB9AC;&#xBC0D; &#xC694;&#xCCAD; &#xBC29;&#xBC95;](../.gitbook/assets/image%20%282%29.png)

### 1. 카메라

1. **메세지큐** 사용: 예측 서빙 모듈및 스트리밍 및 녹화모듈에 동시에 **자원을 공유**하기 위함
2. **sub/pub 방식**을 이용: 두모듈에 동시에 같은 **데이터를 전송**하기위함

### 2. 스트리밍및 녹화 모듈

####    2.1. 송수신 메시지 

| parameter | 설명  |
| :--- | :--- |
| status | 녹화 시작 종료를 알리는 메세 |
| filename | 실험하는 애플리케이션을 알리는 메세 |

####  2.2. 설명 

1. **실시간으로** 데이터를 전송받음
2. 로봇 매니저가 녹화 요청을 보내면 **멀티프로세스를 이용** avi형식으로 데이터를 저장

### 3. Object Detection 서빙 모듈

#### 3.1 송신 메시지 

* 현재 스트리밍되는 앱 화면을 예측하는 **GET 요청 전송**

#### 3.2 수신 메세지 

| parameter  | 설명  |
| :--- | :--- |
| box | detection 결과 만들어진 bounding box 좌표  |

####    3.2. 설명 

1. **Retinanet**을 이용해 예측 모델 제작
2. **flask**를 활용하여 **모델 서빙**
3. 카메라에서 전송하는 메세지 큐로부터 **subscribe하여 데이터를 수신**
4. **Robot manager**로부터 요청을 받으면 카메라로부터 수신되고 있는 영상들을 읽어와 **예측후 좌표 전송** 

