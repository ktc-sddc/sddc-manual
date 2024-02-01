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

# Static Route

***

## 개요

Device 내 등록된 Static Route 정보입니다. Address 와 인터페이스 유형 그리고 상태 정보를 갖고 있으며, Address 정보로 인터페이스 유형을 매핑하는 역할을 합니다.

PBR 연결을 통해 Device 가 연결된 Routing 과 Device 내 Static Route 의 동기화가 자동으로 진행됩니다.

PBR 연결을 통해 Device 를 Routing 에 연결하면 Routing 연결 정보를 바탕으로 Device 내 Static Route 가 생성됩니다. Routing 연결 정보가 변경됨에 따라 Static Route 가 생성 및 삭제 되며 PBR 해제 시 Device 내 생성된 Static Route 가 삭제됩니다.

### 연결된 Routing 과 Static Route 관계

| 연결된 Routing 유형        | Static Route - INT    | Static Route - EXT    |
| --------------------- | --------------------- | --------------------- |
| VPC Peering           | VPC1 하위 연결된 Subnet 목록 | VPC2 하위 연결된 Subnet 목록 |
| Colocation Gateway 연결 | 연결된 Subnet 목록         | 0.0.0.0/0             |
| Cloud Connect 연결      | 연결된 Subnet 목록         | 0.0.0.0/0             |

### Static Route 상태

<table><thead><tr><th width="156">상태(한글)</th><th width="143">상태(영문)</th><th>설명</th></tr></thead><tbody><tr><td>생성중</td><td>CREATING</td><td>생성중인 상태로 생성이 완료되면 IDLE 상태로 전환됩니다.</td></tr><tr><td>정상</td><td>IDLE</td><td>생성이 완료된 상태로 정상 동작중인 상태입니다.</td></tr><tr><td>삭제중</td><td>DELETING</td><td>삭제중인 상태로 삭제가 완료되면 목록에서 제거됩니다.</td></tr><tr><td>실패</td><td>FAILED</td><td>생성 또는 삭제가 실패된 상태입니다.</td></tr></tbody></table>

### 동기화 상태

<table><thead><tr><th width="139">상태(한글)</th><th width="195">상태(영문)</th><th>설명</th></tr></thead><tbody><tr><td>동기화 필요</td><td>SYNC_NECESSARY</td><td>Static Route 수동 동기화가 필요한 상태입니다. 동기화를 통해 Static Route 를 추가하거나 삭제해야합니다.</td></tr><tr><td>동기화 진행중</td><td>SYNC_IN_PROGRESS</td><td>Static Route 동기화가 진행중인 상태입니다. Creating 이나 Deleting 상태인 Static Route 들이 존재합니다. 동기화가 완료되면 동기화 완료 상태로 전환됩니다.</td></tr><tr><td>동기화 완료</td><td>SYNC_COMPLETED</td><td>Static Route 동기화가 완료된 상태입니다. 등록된 Static Route 가 없거나 모든 Static Route 상태가 IDLE 입니다.</td></tr></tbody></table>

## 사용 가이드

### Device 별 Static Route 목록 조회

왼쪽 메뉴에서 'VNF 관리 > VNF > Static Route' 를 클릭하여 Device 별 Static Route 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/static route list.png" alt=""><figcaption></figcaption></figure>

### 동기화

Device 내 Static Route 정보를 수동으로 동기화하는 기능입니다. Device 가 연결된 Routing 과 Device 내 Static Route 의 동기화가 필요한 경우 수동으로 동기화를 진행할 수 있습니다.

> **참고.**
>
> 동기화 완료 상태라면 Static Route 동기화 팝업창 우측 하단의 동기화 버튼이 비활성화 됩니다.

1. 왼쪽 메뉴에서 'VNF 관리 > VNF > Static Route' 를 클릭하여 Device 별 Static Route 목록을 조회합니다.
2. 좌측 상단에 동기화 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/static route need sync list.png" alt=""><figcaption></figcaption></figure>

3. Static Route 목록 현황을 확인합니다. [연결된 Routing 과 Static Route 관계](static-route.md#routing-static-route) 정보와 비교합니다.
4. 추가 내역이나 삭제 내역에 목록이 있다면 우측 하단 동기화 버튼을 클릭하여 수동 동기화를 진행합니다.

<figure><img src="../../.gitbook/assets/static route sync popup.png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. Static Route 가 Deleting 또는 Creating 상태에서 진행되지 않습니다.**
>
> A. 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
