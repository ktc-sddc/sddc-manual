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

# Domain

***

## 개요

Domain 은 한정된 VLAN 자원을 나눠서 관리하는 용도로 사용되며, VLAN Pool 에 대한 정보를 갖고 있습니다 . SDDC Platform 에서는 사전에 등록된 Domain 정보를 조회하는 기능만을 제공합니다.

### 구성

<table><thead><tr><th width="186">속성</th><th>설명</th></tr></thead><tbody><tr><td>Domain 유형</td><td>Domain 의 유형은 Physical, L3 가 있습니다.</td></tr><tr><td>Domain 이름</td><td>Domain 의 이름입니다.</td></tr><tr><td>VLAN Pool</td><td>Domain 이 사용 가능한 VLAN 범위입니다.</td></tr></tbody></table>

## 사용 가이드

### Domain 목록 조회

전체 Domain 목록을 조회하는 기능입니다.

1. 왼쪽 메뉴에서 시스템 관리 > APIC 관리 > Domain 를 클릭하여 Domain 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/image (309).png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. Domain 에 조회되는 목록이 없습니다.**
>
> A. Fabric 동기화 작업이 필요합니다. 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
