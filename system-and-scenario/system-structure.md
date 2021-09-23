---
description: 전체 시스템 구조
---

# System Structure

### **1.** Block Diagram

![&#xC804;&#xCCB4; &#xC2DC;&#xC2A4;&#xD15C; &#xBE14;&#xB85D; &#xB2E4;&#xC774;&#xC5B4;&#xADF8;&#xB7A8;](../.gitbook/assets/image%20%2824%29.png)

1. **Robot Manager**: 모든 모듈을 **통합/제어** 하는 모듈
2. **Image Analyzer**: 휴대폰 **영상**을 **스트리밍/저장** 하고 **클릭 버튼 예측\(Object Detection\)**하는 모듈
3. **Robot Controller**: 로봇이 **클릭할 좌표**를 받아 클락하는 모듈
4. **Packet Collector**: 데이터 송수신시 생기는 **패킷을 캡처 후 저장**하는 모듈
5. **Performance Analyzer**: 수집한 데이터로 Speed Index를 계산하여 **성능을 분석**하는 모듈

### 2. Message Protocol

![](../.gitbook/assets/image%20%2827%29.png)

1.  **Robot Manager**가 각 모듈들에게 **Request**를 보내 동작하는 방식으로 이루어져있음
2. 각 모듈들은 **http 프로토콜**을 이용하여 ,  **JSON Message**로 데이터 전
3. 캡처보드에서 휴대폰 화면을 **스트리밍**
   * **Recorder 모듈**과 **Object Detection 모듈**에게 **실시간**으로 전송함 
   * **TCP를 기반**으로 메시지를 전송하는 프로토콜인 **ZMTQ** \(ZeroMQ Message Transport Protocol\)사용
4. 각 모듈은 필요한 **데이터\(로그들\)** 데이터베이스에 저장



