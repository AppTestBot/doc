---
description: 로봇 제어기와 로봇에대해서 설명합니다.
---

# Robot Controller

![&#xB85C;&#xBD07;\(&#xC88C;\)&#xC640; &#xB85C;&#xBD07; &#xC11C;&#xBCF4;&#xC758; &#xC6C0;&#xC9C1;&#xC784;\(&#xC6B0;\)](../.gitbook/assets/image%20%287%29.png)

### 1. Robot Controller

|  |  |
| :--- | :--- |
|  |  |

* 로봇 매니저로부터 데이터를 전송받음
* 로봇 매니저로부터 전송받은 데이터에따라 다르게 로봇을 다르게 실행시킴
* 로봇 매니저로부터 전송을 요청받는 데이터들
* 로봇의 오픈소스를 모듈이용하기위하여 Node.js를 사용하여 개발

### 2. Robot

* 오픈소스인 Tapster.io로부터 코드와 3D프린터 도면을 이용
* Node.js로 만들어져있음
* 1개의 아두이노와 3개의 서보로 구성되어있음
* 3개의 서보가 0도부터 90도까지 움직이며 이동
