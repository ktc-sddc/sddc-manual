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

# On-Premise와 연결 구성 (1)

## 개요

[다른 네트워크 서버 환경](two-subnet.md)에 추가적으로 SDDC Platform 밖의 네트워크 환경과 통신할 수 있는 연결을 [Cloud Connect](broken-reference)를 활용하여 구성해보도록 하겠습니다.

#### 네트워크 구성도

<figure><img src="../.gitbook/assets/image (513).png" alt=""><figcaption></figcaption></figure>

## 절차

<table><thead><tr><th width="70.33333333333331">No</th><th width="416">설명</th><th>관련 가이드</th></tr></thead><tbody><tr><td>1</td><td>Tenant를 생성합니다.</td><td><a href="../tenant-member.md">Tenant 권한 관리</a></td></tr><tr><td>2</td><td>Tenant 하위에 VPC를 생성합니다.<br>(예시) VPC IP 주소 범위: 10.201.0.0/16</td><td><a href="../network/vpc.md#vpc-1">Network > VPC</a></td></tr><tr><td>3</td><td><p>VPC 하위에 Subnet을 두 개 생성합니다.</p><p>(예시) Subnet-WEB IP 주소 범위: 10.201.1.1/24</p><p>(예시) Subnet-WAS IP 주소 범위: 10.201.2.1/24</p></td><td><a href="../network/subnet.md#subnet-1">Network > Subnet</a></td></tr><tr><td>4</td><td><p>두 개 Subnet이 통신 가능하도록 Routing을 설정합니다.</p><p>(예시) Subnet-WEB &#x3C;-> Subnet-WAS</p></td><td><a href="../network/routing.md#routing-1">Network > Routing</a></td></tr><tr><td></td><td>다수의 Tenant가 공용으로 사용하는 Cloud Connect 사용 신청을 합니다.</td><td><a href="broken-reference">Network > Cloud Connect 신청 관리</a></td></tr><tr><td>5</td><td>외부와 통신을 하고자 하는 서버가 있는 Subnet에 사용 승인을 득한 Cloud Connect를 연결합니다.</td><td><a href="../network/cloud-connect-routing.md#undefined-2">Network > Cloud Connect 연결</a></td></tr><tr><td>6</td><td>각 Server에 연결할 Network Interface를 생성합니다. </td><td><a href="../compute/network-interface.md#network-interface-1">Compute > Network Interface</a></td></tr><tr><td>7</td><td><p>각 Subnet 하위에 Server를 생성합니다.</p><p>예시) Subnet-WEB의 Server: DMZ-WEB</p><p>예시) Subnet-WAS의 Server: WAS01</p></td><td><a href="../compute/server.md#server-3">Compute > Server</a></td></tr><tr><td>8</td><td>Cloud Connect를 연결한 Subnet에 생성한 Server Terminal에 접속하여 외부 네트워크에 존재하는 서버와 통신이 가능한지 확인합니다.</td><td><a href="../compute/server.md#server-terminal">Compute > Server</a></td></tr></tbody></table>
