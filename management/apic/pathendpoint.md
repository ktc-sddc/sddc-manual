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

# PathEndpoint

***

## 개요

PathEndpoint 는 Leaf 스위치 내 포트 정보를 의미합니다. SDDC Platform 에서 PathEndpoint 를 관리하는 기능을 제공하지 않고, 사전에 등록된 정보를 조회하는 기능을 제공합니다.

### 구성

<table><thead><tr><th width="161">속성</th><th>설명</th></tr></thead><tbody><tr><td>유형</td><td>PathEndpoint 의 유형으로, PORT와 VPC가 있습니다.<br>PORT는 물리적인 Port를 의미하고, VPC는 Virtual Port Channel을 의미합니다.</td></tr><tr><td>Pod</td><td>PathEndpoint 가 위치한 Pod 정보입니다.<br>Pod는 Spine Switch와 Leaf Switch의 세트입니다.</td></tr><tr><td>Leaf</td><td>PathEndpoint 가 위치한 Leaf 정보입니다.</td></tr><tr><td>이름</td><td>PathEndpoint 의 이름입니다.</td></tr><tr><td>식별자</td><td>PathEndpoint 의 식별자입니다. 다른 PathEndpoint 와 구분되는 유일한 값을 갖습니다.</td></tr><tr><td><a href="pathendpoint.md#pathendpoint">상태</a></td><td>PathEndpoint 의 상태입니다. UP, DOWN, DISABLED_USING_PC, DISABLED_UNCALLED 4가 상태가 있습니다.</td></tr></tbody></table>

### PathEndpoint 상태

<table><thead><tr><th width="180">상태(한글)</th><th width="218">상태(영문)</th><th>설명</th></tr></thead><tbody><tr><td>활성화</td><td>UP</td><td>활성화</td></tr><tr><td>비활성화</td><td>DOWN</td><td>비활성화</td></tr><tr><td>Port Channel 사용</td><td>DISABLED_USING_PC</td><td>Port Channel 사용</td></tr><tr><td>케이블 연결 안됨</td><td>DISABLED_UNCALLED</td><td>케이블 연결 안됨</td></tr></tbody></table>

## 사용 가이드

### PathEndpoint 목록 조회

전체 PathEndpoint 목록을 조회하는 기능입니다.

1. 왼쪽 메뉴에서 시스템 관리 > APIC 관리 > PathEndpoint 를 클릭하여 PathEndpoint 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/image (310).png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. PathEndpoint 에 조회되는 목록이 없습니다.**
>
> A. Fabric 동기화 작업이 필요합니다. 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
