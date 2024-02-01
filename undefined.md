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

# 대시보드

***

## 개요

Tenant에 속한 리소스 현황, Network 트래픽 정보 및 Topology 연결 관계를 확인 할 수 있습니다.

#### 대시보드 종류

다음 3가지 종류의 대시보드가 존재합니다.

<table><thead><tr><th width="146">종류</th><th>설명</th></tr></thead><tbody><tr><td>Summary</td><td>Server, Block Storage, VPC, Subnet 및 연결 관계 리소스 현황을 확인 할 수 있습니다.</td></tr><tr><td>Metering</td><td>Colocation Gateway, Cloud Connect의 오늘, 최근 30일, 시간별 트래픽 발생 현황, 일별 트래픽 발생 현황을 확인 할 수 있습니다.</td></tr><tr><td>Topology</td><td>Tenant에 속한 VPC, Subnet, Network Interface, Server 정보 및 연결 관계를 확인 할 수 있습니다.</td></tr></tbody></table>

## 사용자 가이드

### Summary

현재 선택된 Tenant의 리소스 정보를 확인 할 수 있습니다.

<figure><img src=".gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

#### Summary 영역 설명

<table><thead><tr><th width="237">영역</th><th>설명</th></tr></thead><tbody><tr><td>Server</td><td>사용 중인 Server 상태 및 Flavor 현황입니다.</td></tr><tr><td>Block Storage</td><td>Server에 연결된 Block Storage 현황입니다.</td></tr><tr><td>Volume Snapshot</td><td>특정 시점의 Volume Snapshot 현황입니다.</td></tr><tr><td>Security Group</td><td>Server의 네트워크 트래픽을 제어할 수 있는 가상의 방화벽 현황입니다.</td></tr><tr><td>VPC</td><td>논리적으로 격리된 가상의 네트워크 현황입니다.</td></tr><tr><td>VPC Peering</td><td>서로 다른 VPC 내 Subnet 연결 현황입니다.</td></tr><tr><td>Subnet</td><td>각 VPC 내 Subnet 현황입니다.</td></tr><tr><td>Routing</td><td>동일한 VPC 내 Subnet 연결 현황입니다.</td></tr><tr><td>Colocation Gateway</td><td>플랫폼 네트워크와 고객 네트워크 간의 허브 현황입니다.</td></tr><tr><td>Colocation Gateway 연결</td><td>플랫폼 네트워크와 고객 네트워크 간의 허연 연결 현황입니다.</td></tr><tr><td>Cloud Connect</td><td>외부 네트워크와의 연결을 위해 공용으로 사용 가능한 Gateway 현황입니다.</td></tr><tr><td>Cloud Connect 연결</td><td>외부 네트워크와의 연결을 위해 공용으로 사용 가능한 Gateway 연결 현황입니다.</td></tr><tr><td>vFW</td><td>vFW 별 정책 현황입니다.</td></tr></tbody></table>

### Metering

#### 제공 중인 Metering 유형(2023.08 기준)

* **Colocation Gateway**: Colocation Gateway를 통한 네트워크 트래픽량 정보 제공
* **Cloud Gateway**: Cloud Gateway를 통한 네트워크 트래픽량 정보 제공

#### Metering 영역 설명

<table><thead><tr><th width="197">영역</th><th>설명</th></tr></thead><tbody><tr><td>Today</td><td>금일 Inbound/Outbound 트래픽 정보를 확인 할 수 있습니다.</td></tr><tr><td>최근 30일</td><td>최근 30일 간의 Inbound/Outbound 트래픽 정보를 확인 할 수 있습니다.</td></tr><tr><td>Today 시간별</td><td>시간별 트래픽 발생 현황을 확인 할 수 있습니다.</td></tr><tr><td>최근 30일 일별</td><td>일별 트래픽 발생 현황을 확인 할 수 있습니다.</td></tr></tbody></table>

> **참고**
>
> * 트래픽 단위를 bytes와 MB로 변환이 가능합니다.
> * 최근 30일 일별 트래픽의 경우 원하는 기간으로도 조회가 가능합니다.

#### Metering 조회 - Colocation Gateway

1. Today, 최근 30일 정보를 확인합니다.

<figure><img src=".gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

2. Today 시간별 트래픽 발생 현황을 확인합니다.

<figure><img src=".gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

3. 최근 30일 일별 트래픽 발생 현황을 확인합니다.

<figure><img src=".gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

### Topology

현재 선택되어 있는 Tenant의 네트워크 형상을 확인 할 수 있습니다.

> **참고**
>
> * Network Interface를 마우스 오버하면 Server 정보를 확인 할 수 있습니다.
> * 그룹(VPC, Subnet)과 오브젝트(Colocation Gateway)을 클릭하면, 클릭한 리소스의 연결관계를 확인할 수 있습니다. 또는 토폴로지 좌측 하단의 눈 표시 버튼을 클릭하여 전체 리소스 연결관계를 확인할 수 있습니다.

<figure><img src=".gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

#### Topology 영역

다음 4가지 영역으로 나뉩니다.

<table><thead><tr><th width="146">종류</th><th>설명</th></tr></thead><tbody><tr><td>Pane 영역</td><td>현재 선택된 Tenant의 네트워크 현황을 Topology 형태로 확인 할 수 있습니다.</td></tr><tr><td>Left Bar 영역</td><td><p>각 그룹, 오브젝트, 연결 관계에 대한 아이콘을 나타냅니다.</p><ul><li><p>그룹</p><ul><li>VPC : Tenant 내에 논리적으로 격리된 네트워크 공간입니다.</li><li>Subnet : VPC 내에 세분화된 네트워크 격리 공간입니다.</li></ul></li><li><p>오브젝트</p><ul><li>Colocation Gateway : 플랫폼 네트워크과 고객 네트워크 간의 연결 허브 역할을 합니다.</li><li>Network Interface : Server가 Subnet을 통해 내/외부로 통신 할 수 있는 역할을 합니다.</li></ul></li><li><p>연결 관계</p><ul><li>Colocation Gateway와 Subnet과 연결을 빨간색 선으로 표시합니다.</li><li>서로 다른 VPC에 속한 Subnet과 Subnet의 연결을 파란색 선으로 표시합니다.</li><li>동일한 VPC에 속한 Subnet과 Subnet의 연결을 초록색 선으로 표시합니다.</li></ul></li></ul></td></tr><tr><td>Minimap 영역</td><td>현재 선택된 Tenant의 네트워크 현황을 축소된 미니맵 형태로 확인 할 수 있습니다.</td></tr><tr><td>Control 영역</td><td><p>6개의 기능을 갖고 있습니다.</p><ul><li>+ 버튼 : Topology를 확대 시킵니다.</li><li>- 버튼 : Topology를 축소 시킵니다.</li><li>맞춤 버튼 : Topology를 화면 크기에 맞게 맞춥니다.</li><li>잠금 버튼 : Topology의 각 요소들의 클릭드래그 기능을 잠금/해제 합니다.</li><li>눈 표시 버튼 : 각 요소들의 연결 관계를 show/hide 처리합니다.</li><li>새로고침 버튼 : Topology를 새로고침 합니다.</li></ul></td></tr></tbody></table>

## FAQ

> **Q. 전체 Tenant 대시보드는 존재하지 않나요?**
>
> A. 향후 기능 개발을 통해 고도화 예정입니다.
