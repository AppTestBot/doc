---
description: 로봇 제어기와 로봇에대해서 설명합니다.
---

# Robot Controller

### 1. Robot Controller

####    1.1 요청 파라미터 설명 

<table>
  <thead>
    <tr>
      <th style="text-align:left">parameter</th>
      <th style="text-align:left">&#xC124;&#xBA85;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">source</td>
      <td style="text-align:left">
        <p>&#xC2E4;&#xD5D8;&#xC758; &#xC885;&#xB958;</p>
        <ul>
          <li>click test: &#xB85C;&#xBD07;&#xD130;&#xCE58; &#xD14C;&#xC2A4;&#xD2B8;</li>
          <li>experiment: &#xB85C;&#xBD07; &#xC2E4;&#xD5D8; &#xD14C;&#xC2A4;&#xD2B8;</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">status</td>
      <td style="text-align:left">
        <p>&#xC560;&#xD50C;&#xB9AC;&#xCF00;&#xC774;&#xC158; &#xC131;&#xB2A5; &#xBD84;&#xC11D;&#xC885;&#xB958;</p>
        <ul>
          <li>start: &#xC2E4;&#xD5D8;&#xC2DC;&#xC791; &#xC2DC;&#xAC04;&#xC744; &#xAE30;&#xB85D;</li>
          <li>appexecute: &#xC560;&#xD50C;&#xB9AC;&#xCF00;&#xC774;&#xC158; &#xC2E4;&#xD589;,
            &#xC560;&#xD50C;&#xB9AC;&#xCF00;&#xC774;&#xC158; &#xC2E4;&#xD589;&#xC2DC;&#xAC04;
            &#xAE30;&#xB85D;</li>
          <li>ongoing: &#xCE74;&#xBA54;&#xB77C;&#xC5D0;&#xAC8C; &#xC5B4;&#xB514;&#xB97C;
            &#xD074;&#xB9AD;&#xD560;&#xC9C0; &#xC694;&#xCCAD;</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">starttime</td>
      <td style="text-align:left">&#xC571; &#xD130;&#xCE58;&#xC2DC;&#xAE30; &#xBC0F; &#xC571; &#xC2E4;&#xD5D8;
        &#xC2DC;&#xC791; &#xC2DC;&#xAC04;&#xC744; &#xAE30;&#xB85D;</td>
    </tr>
    <tr>
      <td style="text-align:left">xaxis, yaxis</td>
      <td style="text-align:left">Button Predict Module&#xB85C;&#xBD80;&#xD130; &#xB370;&#xC774;&#xD130;
        &#xC804;&#xC1A1;&#xBC1B;&#xC744;&#xB54C; &#xC0AC;</td>
    </tr>
  </tbody>
</table>

####   1.2 Robot Controller 동작 설명 

1. **Robot Manager**로부터 실험 시작 명령을 받아 **Object Detection**에 **클릭 좌표를 요청**하는 역할
2. 클릭 좌표를 로봇에 **명령**을 내려 **클릭**하는역할
3. **클릭 시간**을 **기록** 하는 역할 
4. **로봇의 오픈소스**를 이용하기위하여 **Node.js**를 사용하여 개발

### 2. Robot

![&#xB85C;&#xBD07;\(&#xC88C;\)&#xC640; &#xB85C;&#xBD07; &#xC11C;&#xBCF4;&#xC758; &#xC6C0;&#xC9C1;&#xC784;\(&#xC6B0;\)](../.gitbook/assets/image%20%288%29.png)

1. 오픈소스인 **Tapster.io**로부터 코드와 **3D프린터 도면**을 이용
2. **1개의 아두이노**와 **3개의 서보**로 구성되어있음
3. 3개의 서보가 0도부터 90도까지 움직이며 **x, y, z 축으로 이동** 

