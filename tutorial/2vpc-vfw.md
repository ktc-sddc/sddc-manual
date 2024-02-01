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

# vFW을 활용한 네트워크 구성

## 개요

다양한 통신 구간에 방화벽 설정이 가능하나, 이번 튜토리얼에서는 VPC 간 통신을 구성하고 그 구간에 방화벽을 구성해보도록 하겠습니다.&#x20;

#### 네트워크 구성도

<figure><img src="../.gitbook/assets/image (515).png" alt=""><figcaption></figcaption></figure>

## 절차

<table><thead><tr><th width="70.33333333333331">No</th><th width="416">설명</th><th>관련 가이드</th></tr></thead><tbody><tr><td>1</td><td>Tenant를 생성합니다.</td><td><a href="../tenant-member.md">Tenant 권한 관리</a></td></tr><tr><td>2</td><td>Tenant 하위에 서로 다른 VPC를 2개 생성합니다.<br>(예시) VPC-WEB IP 주소 범위: 10.201.0.0/16<br>(예시) VPC-WAS IP 주소 범위: 192.168.0.0/16</td><td><a href="../network/vpc.md#vpc-1">Network > VPC</a></td></tr><tr><td>3</td><td><p>각 VPC 하위에 Subnet을 한 개씩 생성합니다.</p><p>(예시) Subnet-WEB IP 주소 범위: 10.201.1.1/24</p><p>(예시) Subnet-WAS IP 주소 범위: 192.168.10.1/24</p></td><td><a href="../network/subnet.md#subnet-1">Network > Subnet</a></td></tr><tr><td>4</td><td><p>VPC 하위의 각 Subnet이 통신 가능하도록 VPC Peering을 생성합니다.</p><p>(예시) VPC1: VPC-WEB, Subnet: Subnet-WEB<br>(예시) VPC2: VPC-WAS, Subnet: Subnet-WAS</p></td><td><a href="../network/routing.md#routing-1">Network > Routing</a></td></tr><tr><td>5</td><td>각 Server에 연결할 Network Interface를 생성합니다. </td><td><a href="../compute/network-interface.md#network-interface-1">Compute > Network Interface</a></td></tr><tr><td>6</td><td><p>각 Subnet 하위에 Server를 생성합니다.</p><p>예시) Subnet-WEB의 Server: DMZ-WEB</p><p>예시) Subnet-WAS의 Server: WAS01</p></td><td><a href="../compute/server.md#server-3">Compute > Server</a></td></tr><tr><td>7</td><td>운영자에게 방화벽 생성을 요청합니다(방화벽 생성을 원하는 Tenant와 VPC 정보가 필요합니다).</td><td><a href="../nov/firewall.md">NFV > vFW</a></td></tr><tr><td>8</td><td><p>방화벽 정책을 추가합니다.</p><p>Source IP와 Destination IP에 원하는 Subnet을 입력하고, 차단 혹은 허용을 원하는 Service port 번호를 입력합니다. 이후 차단 여부를 선택 후, 정책을 생성합니다.<br>(예시) Interface 유형: INT, 입력 유형: Subnet, IP Address: 10.201.1.1/24<br>(예시) Interface 유형: EXT, 입력 유형: Subnet, IP Address: 192.168.10.1/24<br>(예시) Protocol: TCP, Port: 22, 허용</p></td><td><a href="../nov/firewall.md#vfw-2">NFV > vFW</a></td></tr><tr><td>9</td><td>VPC Peering에 포함된 Subnet에 생성한 Server Terminal에 접속하여 서버 간 통신을 확인합니다.</td><td><a href="../compute/server.md#server-terminal">Compute > Server</a></td></tr></tbody></table>
