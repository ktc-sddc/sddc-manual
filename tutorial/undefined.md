# 단일 네트워크 서버 환경 구성

## 개요

외부와 격리된 단일 네트워크(Subnet)에 서로 통신이 가능한 두 개의 서버를 생성해보도록 합니다.

#### 네트워크 구성도

<figure><img src="../.gitbook/assets/image (512).png" alt=""><figcaption></figcaption></figure>

## 절차

<table><thead><tr><th width="68.33333333333331">No</th><th width="418">설명</th><th>관련 가이드</th></tr></thead><tbody><tr><td>1</td><td>Tenant를 생성합니다.</td><td><a href="../tenant-member.md">Tenant 권한 관리</a></td></tr><tr><td>2</td><td>Tenant 하위에 VPC를 생성합니다.<br>(예시) VPC IP 주소 범위: 10.220.0.0/16 </td><td><a href="../network/vpc.md#vpc-1">Network > VPC</a></td></tr><tr><td>3</td><td><p>VPC 하위에 Subnet을 생성합니다. </p><p>(예시) Subnet-Local IP 주소 범위: 10.220.1.1/24</p></td><td><a href="../network/subnet.md#subnet-1">Network > Subnet</a></td></tr><tr><td>4</td><td>각 Server에 연결할 Network Interface를 생성합니다. </td><td><a href="../compute/network-interface.md#network-interface-1">Compute > Network Interface</a></td></tr><tr><td>5</td><td>Subnet 하위에 Server를 두 개 생성합니다.</td><td><a href="../compute/server.md#server-3">Compute > Server</a></td></tr><tr><td>6</td><td>Server Terminal에 접속하여 두 Server 간의 통신을 확인합니다.</td><td><a href="../compute/server.md#server-terminal">Compute > Server</a></td></tr></tbody></table>
