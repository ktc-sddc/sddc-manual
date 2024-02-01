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

# Gateway Info

***

## 개요

Gateway Info 는 Gateway 생성에 필요한 정보를 관리합니다.

Gateway Info 생성 시 Gateway에서 사용할 네트워크 인터페이스를 선택하게 되는데, 지원하는 인터페이스 유형은 다음과 같습니다.

#### Interface 유형

<table><thead><tr><th width="224.4782608695652">유형</th><th>설명</th></tr></thead><tbody><tr><td>Routed</td><td>L3 Switch Port 의 Routed Interface 유형으로 자세한 내용은 <a href="https://www.cisco.com/c/en/us/td/docs/switches/datacenter/nexus5000/sw/interfaces/521_N11/b_5k_Interfaces_Config_Guide_Release_521N11/b_5k_Interfaces_Config_Guide_Release_521N11_chapter_011.pdf">여기</a>를 참고해주시기 바랍니다.</td></tr><tr><td>Sub Interface</td><td>L3 Switch Port 의 Sub Interface 유형으로 자세한 내용은 <a href="https://www.cisco.com/c/en/us/td/docs/switches/datacenter/nexus5000/sw/interfaces/521_N11/b_5k_Interfaces_Config_Guide_Release_521N11/b_5k_Interfaces_Config_Guide_Release_521N11_chapter_011.pdf">여기</a>를 참고해주시기 바랍니다.</td></tr><tr><td>SVI</td><td>L3 Switch Port 의 SVI(Switch Virtual Interface) 유형으로 자세한 내용은 <a href="https://www.cisco.com/c/en/us/td/docs/switches/datacenter/nexus5000/sw/interfaces/521_N11/b_5k_Interfaces_Config_Guide_Release_521N11/b_5k_Interfaces_Config_Guide_Release_521N11_chapter_011.pdf">여기</a>를 참고해주시기 바랍니다.</td></tr></tbody></table>

#### Gateway 유형

<table><thead><tr><th width="224.4782608695652">유형</th><th width="357">Gateway</th><th>중복 사용 여부</th></tr></thead><tbody><tr><td>Colocation</td><td>Colocation Gateway </td><td>X</td></tr><tr><td>Shared Colocation</td><td>Shared Colocation Gateway </td><td>X</td></tr><tr><td>Internet</td><td>Internet Gateway</td><td>O</td></tr><tr><td>NAT(준비중)</td><td>NAT Gateway</td><td>O</td></tr></tbody></table>

#### Gateway Info 정보 활용 예시 (Gateway 생성 시)

아래 테이블과 같이 구성된 Gateway Info 'GW-Info' 가 있습니다.

<table><thead><tr><th width="227">속성</th><th>값</th></tr></thead><tbody><tr><td>Gateway Info 이름</td><td>GW-Info</td></tr><tr><td>Gateway 유형</td><td>Colocation Gateway</td></tr><tr><td>Interface 유형</td><td>SVI</td></tr><tr><td>PathGroup 이름</td><td>EXT-PG</td></tr><tr><td>vlan 번호</td><td>1000</td></tr><tr><td>PathEndpoint 구성1<br>(PathEndpoint 구성 내역)</td><td><p>유형 : PORT</p><p>PathEndpoint : PathEp1<br>IP Address 1 : 10.20.30.0/24</p></td></tr><tr><td>Node 정보1<br>(Node 정보)</td><td><p>이름 : Node1<br>Router Id : 1.1.1.1<br>Static Routes</p><ul><li>Static Route Ip: 10.0.0.0/8</li><li>Next Hop Ip: 10.20.30.1/24</li></ul></td></tr></tbody></table>

> * GW-Info 의 Gatetway 유형이 Colocation Gateway 이므로 [Colocation Gateway 생성](https://gitlab.com/sddcmanager/sddc-manual/-/blob/main/sdn/broken-reference/README.md) 시 사용 가능합니다.
> * GW-Info 를 이용하여 Colocation Gateway 'EXT-GW' 를 생성하면, 'EXT-GW' 와 [Colocation Gateway 연결](../network/colocation-gateway-routing.md)을 통해 10.0.0.0/8 대역을 가진 외부 네트워크와 통신이 가능하게 됩니다.&#x20;
> * 이 때 Border Leaf 는 Node1 이 되고, 외부 네트워크와 접점이 되는 인터페이스는 PathEp1 이 됩니다. 그리고 이를 통해 나가는 Traffic 은 1000번 vlan 으로 Encap 됩니다.&#x20;
> * **단, 외부 네트워크에서 ACI Network 를 인식할 수 있도록 라우팅 테이블을 설정하는 사전 작업이 필요합니다.**



## 사용 가이드

### Gateway Info 목록 조회

전체 Gateway Info 목록을 조회하는 기능입니다.

메뉴에서 SDN 관리 > Gateway Info 를 클릭하여 Gateway Info 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (239).png" alt=""><figcaption></figcaption></figure>

### Gateway Info 생성

Gateway 생성 시 필요한 정보를 생성하는 기능입니다. Gateway Info를 생성하기 위해선 Gateway 유형의 [PathGroup](pathgroup.md) 이 사전에 등록되어 있어야 합니다.

1. 메뉴에서 SDN 관리 > Gateway Info 를 클릭하여 Gateway Info 목록을 조회합니다.
2. 상단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (240).png" alt=""><figcaption></figcaption></figure>

3. Gateway Info 생성 정보를 입력합니다.
   * Gateway Info 이름: 생성할 Gateway Info 의 이름입니다.
   * Gateway 유형: Gateway Info 가 사용될 Gateway 유형입니다.
   * Interface 유형: Gateway 의 네트워크 인터페이스 유형 정보입니다. Routed, SVI, Sub Interface 중 선택 가능하며, SVI 나 Sub Interface를 선택하는 경우, vlan 번호를 반드시 입력해야합니다.
   * PathGroup 이름: Gateway Info 와 연관된 PathGroup 이름입니다.
   * PathEndpoint 구성: PathGroup 을 선택하면 [PathEndpoint](../management/apic/pathendpoint.md) 구성 내역이 자동으로 채워집니다. 유형이 Port 인 경우 IP Address 를 1개 입력하고, VPC 인 경우 2개를 입력합니다.
   * Node 구성: PathGroup 을 선택하면 Node구성 내역이 자동으로 채워집니다.
     * Router Id : Route Id 는 고유 번호로 Gateway Info 간 에도 중복되지 않도록 합니다.
     * Static Routes : Static Route 정보를 입력합니다.
       1. Static Routes 입력 버튼을 클릭하면 Static Routes 입력 팝업창이 나타납니다.
       2. Static Route Ip와 Next Hop IP 정보를 입력합니다.
       3.  입력이 완료되면, 팝업 창 우측 하단의 저장 버튼을 클릭합니다.

           <figure><img src="../.gitbook/assets/image (241).png" alt=""><figcaption></figcaption></figure>
       4. Static Route 입력 팝업창이 닫히고, Gateway Info 생성 팝업창에서 Static Routes 입력 여부를 확인할 수 있습니다.(미입력 / n개 입력)
4. 팝업창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (242).png" alt=""><figcaption></figcaption></figure>

5. Gateway Info 목록에서 생성한 Gateway Info 를 확인합니다.

### Gateway Info 수정

Gateway Info 를 수정하는 기능입니다.

1. 메뉴에서 SDN 관리 > Gateway Info 를 클릭하여 Gateway Info 목록을 조회합니다.
2. 상단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (244).png" alt=""><figcaption></figcaption></figure>

3. Gateway Info 수정 정보를 입력합니다. [Gateway Info 생성](gateway-info.md#gateway-info-1)을 참고하십시오.
   * Gateway Info를 사용 중인 Gateway가 존재하는 경우, Static Routes 정보만 수정 가능합니다.
   * Gateway Info를 사용중인 Gateway가 없는 경우, 모든 입력 정보를 수정할 수 있습니다.
4. 팝업창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (243).png" alt=""><figcaption></figcaption></figure>

5. Gateway Info 목록에서 수정한 Gateway Info 를 확인합니다.

### Gateway Info 삭제

Gatway Info 를 삭제하는 기능입니다.

{% hint style="info" %}
**참고.**

* '**사용 중'** 상태의 Gateway Info 는 삭제할 수 없습니다.
{% endhint %}

1. 메뉴에서 SDN 관리 > Gateway Info 를 클릭하여 Gateway Info 목록을 조회합니다.
2. 상단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (245).png" alt=""><figcaption></figcaption></figure>

3. 팝업창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (246).png" alt="" width="375"><figcaption></figcaption></figure>

4. Gateway Info 목록에서 삭제한 Gateway Info 를 확인합니다.

## FAQ

> **Q. Gateway Info 생성이 되지 않습니다.**
>
> A. [Gateway Info 생성](gateway-info.md#gateway-info) 을 참고해주시기 바랍니다. 만약 해결 되지 않는다면 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. Gateway Info 삭제가 되지 않습니다.**
>
> A. [Gateway Info 삭제](gateway-info.md#2.-gateway-info-2) 을 참고해주시기 바랍니다. 만약 해결 되지 않는다면 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.G
