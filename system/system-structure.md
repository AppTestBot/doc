---
description: 전체 시스템 구조
---

# System Structure

### **1.** Block Diagram

![](../.gitbook/assets/image%20%2810%29.png)

1.  Robot Manager가 각 모듈들에게 Request를 보내 동작하는 방식으로 이루어져있음
2. 각 모듈들은 http프로토콜을 이용하여 ,  json 형식으로 데이터를 통신
3. 캡처보드에서 휴대폰 화면을 스트리밍하여 Recorder 모듈과 Click Predictor 모듈에게 실시간으로 전송함 이때 메세지 tcp가 메시지를 전송하는 프로토콜인 zmtp \(zeromq message transport protocol\)사용
4. 각 모듈은 필요한 데이터\(로그들\) 데이터베이스에 저장
5. Performance Analyzer가 데이터 베이스의 모든 경로를 읽어와 성능을 계산하여 최종결과를 저장
6. 저장된 결과는 시각화 자료로 사용됨

### 2. Message Protocol

![](../.gitbook/assets/image%20%287%29.png)



