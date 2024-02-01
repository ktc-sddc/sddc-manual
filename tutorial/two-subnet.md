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

# 다른 네트워크 서버 환경 구성

## 개요

IP 대역이 다른 두 개의 Subnet에 각각 Server를 생성하고, Server 간에 통신이 가능하도록 해보겠습니다.\
외부와 연결되는 서버(DMZ)와 내부에 격리된 서버(Legacy) 구성할 때 활용할 수 있는 사례입니다.

#### 네트워크 구성도

<figure><img src="../.gitbook/assets/image (510).png" alt=""><figcaption></figcaption></figure>

## 절차

<table><thead><tr><th width="70.33333333333331">No</th><th width="417">설명</th><th>관련 가이드</th></tr></thead><tbody><tr><td>1</td><td>Tenant를 생성합니다.</td><td><a href="../tenant-member.md">Tenant 권한 관리</a></td></tr><tr><td>2</td><td>Tenant 하위에 VPC를 생성합니다.<br>(예시) VPC IP 주소 범위: 10.201.0.0/16</td><td><a href="../network/vpc.md#vpc-1">Network > VPC</a></td></tr><tr><td>3</td><td><p>VPC 하위에 Subnet을 두 개 생성합니다.</p><p>(예시) Subnet-WEB IP 주소 범위: 10.201.1.1/24</p><p>(예시) Subnet-WAS IP 주소 범위: 10.201.2.1/24</p></td><td><a href="../network/subnet.md#subnet-1">Network > Subnet</a></td></tr><tr><td>4</td><td><p>두 개 Subnet이 통신 가능하도록 Routing을 설정합니다.</p><p>(예시) 출발지: Subnet-WEB, 목적지: Subnet-WAS</p></td><td><a href="../network/routing.md#routing-1">Network > Routing</a></td></tr><tr><td>5</td><td>각 Server에 연결할 Network Interface를 생성합니다. </td><td><a href="../compute/network-interface.md#network-interface-1">Compute > Network Interface</a></td></tr><tr><td>6</td><td><p>각 Subnet 하위에 Server를 생성합니다.</p><p>예시) Subnet-WEB의 Server: DMZ-WEB</p><p>예시) Subnet-WAS의 Server: WAS01</p></td><td><a href="../compute/server.md#server-3">Compute > Server</a></td></tr><tr><td>7</td><td>각 서버의 Terminal에 접속하여 Routing 설정한 방향으로 통신이 가능한지 확인합니다.</td><td><a href="../compute/server.md#server-terminal">Compute > Server</a></td></tr></tbody></table>
