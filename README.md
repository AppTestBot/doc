---
description: 모바일 애플리케이션의 성능 테스트를 위한 응용 프로그램입니다.
---

# INTRODUCE

## 1. 목적 및 기능  

### 1. 목적: 모바일 애플리케이션의 성능을 테스트 하는 로봇

* **User Experience 관점**의 **성능을 테스트**하는 **로봇**
* [연구의 필요성](why-need-1/need.md) 및 [풀고자 하는문제](why-need-1/undefined.md)

### 2. 주요 기능

1. 각 모듈의 통합 동작 제어 기능\([Robot Manager](system-and-scenario/test-manager.md)\)
2. 로봇 팔의 앱 버튼 터치 기능 \([Robot Controller](system-and-scenario/robot-controller.md)\)
3. 다중 스트리밍 기능 \([Image Analyzer](system-and-scenario/appbutton-predictor.md)\)
   * Object Detection 및 서빙
   * 녹화 및 스트리밍
4. 성능 분석기능\([Performance Analyzer](system-and-scenario/performance-analyzer.md)\)
   * Speed Index의 Application 구현 적용 
   * 서빙 모듈 구현 

## 2. 주요 시스템 \([System Structure](system-and-scenario/system-structure.md)\)

![&#xB85C;&#xBD07; &#xD14C;&#xC2A4;&#xD2B8; &#xC2DC;&#xC2A4;&#xD15C;](.gitbook/assets/image%20%2821%29.png)

## 3. 주요 결과  

### 1. 로봇 평가\([Robot Accuracy](evaluation-and-analysis/untitled-1.md)\)

* 로봇 클릭 정확도
* Object Detection 정확도
* 장면 탐지 정확도 

### 2. 애플리케이션 분석 결과 \([App Analysis Result](evaluation-and-analysis/app-analysis-result.md)\)

* 스피드인덱스와 로딩 시간의 관계
* 앱과 네트워크의 관계
* 앱과 UI/Image의 관계 

## 4. 개선 사항\([Improvements](develop-method.md)\)

* 구현에서의 개선 사항
* 설계에서의 개선 사항 



