---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Flavor 관리

***

## 개요

컴퓨팅, 메모리와 같이 자주 사용하는 서버 구성 요소 정보를 미리 정의하는 서비스입니다.

서버를 생성할 때, 미리 정의한 Flavor를 이용해 동일한 타입의 서버를 간편하게 구성하여 생성할 수 있습니다.&#x20;

### 서버 타입 종류

서버 타입은 CPU/RAM으로 구성되어 있으며, 서비스 규모와 목적에 따라 4가지 서버 타입을 제공합니다.

<table><thead><tr><th width="156">서버타입</th><th width="418">특징</th><th>추천 용도</th></tr></thead><tbody><tr><td>Compact</td><td><p>vCPU가 2 core 이하인 저사양 서버입니다.</p><p>운영하는 서비스가 높은 성능을 요구하지 않고, 서버 운영 비용 부담을 덜고자 하는 분들에게 적합합니다.</p></td><td>개발 테스트 서버</td></tr><tr><td>Standard<br>(1:4)</td><td>범용 모델로 다양한 워크 로드에 적합한 서비스를 제공합니다.</td><td>중/대규모 모바일 및 웹 서비스 운영</td></tr><tr><td>High_Memory<br>(1:8)</td><td>대용량 데이터 처리 등과 같은 메모리 집약적 워크 로드에 적합한 서비스를 제공합니다.</td><td>고성능 데이터베이스 서버</td></tr><tr><td>High_CPU<br>(1:2)</td><td>CPU 집약형 모델로<br>많은 연산이 필요한 업무에 최적화된 서버입니다.</td><td>게임 서버</td></tr></tbody></table>

## FAQ

> **Q. 사용하고자 하는 Flavor가 없습니다. 서버 타입을 어떻게 추가하나요?**
>
> **A.** 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
