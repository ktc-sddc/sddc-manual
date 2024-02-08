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

# PathGroup

***

## 개요

PathGroup 은 네트워크 리소스 생성에 필요한 물리 구성 정보를 서비스 목적에 맞게 그룹화하여 관리합니다.

* 네트워크 리소스&#x20;
  * [Subnet](../network/subnet.md), [Colocation Gateway](colocation-gateway.md), [Shared Colocation Gateway](cloud-connect.md), Internet Gateway, NFV, NAS
* 물리 구성 정보&#x20;
  * [Domain](../management/apic/domain.md), [PathEndpoint](../management/apic/pathendpoint.md)

### PathGroup 유형

PathGroup 유형은 서비스 생성 시 참고할 물리 구성 정보를 의미하며, 생성 가능한 PathGroup 유형에는 Subnet, NFV, Colocation Gateway등이 있습니다.&#x20;

예로 Subnet 유형의 PathGroup 은 Subnet 생성 시 사용됩니다. 각 유형별로 연결 가능한 Domain 유형은 다음과 같습니다.

<table><thead><tr><th width="364.8955223880597">PathGroup 유형</th><th>Domain 유형</th></tr></thead><tbody><tr><td>Subnet</td><td>Physical</td></tr><tr><td>NFV</td><td>Physical</td></tr><tr><td>NAS</td><td>Physical</td></tr><tr><td>Colocation Gateway</td><td>L3</td></tr><tr><td>Shared Colocation Gateway</td><td>L3</td></tr><tr><td>Internet Gateway</td><td>L3</td></tr><tr><td>NAT Gateway(준비중)</td><td>L3</td></tr></tbody></table>



## 사용 가이드

### PathGroup 목록 조회

전체 PathGroup 목록을 조회하는 기능입니다.

메뉴에서 SDN 관리 > PathGroup을 클릭하여 PathGroup 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### PathGroup 생성

PathGroup을 생성하는 기능입니다.

{% hint style="info" %}
**참고.**

* PathGroup을 구성하기 위해서는 SDDC Platform의 인프라 정보를 사전에 계획해야 합니다.
* 생성 화면에 Domain, PathEndpoint 정보가 조회되지 않는다면, Fabric 동기화를 통해 Domain, PathEndpoint 정보를 등록하는 작업이 필요합니다.
* Fabric 동기화 작업이 필요하다면 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
{% endhint %}

1. 메뉴에서 SDN 관리 > PathGroup을 클릭하여 PathGroup 목록을 조회합니다.
2. 상단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

3. PathGroup 생성을 위한 필요정보를 입력합니다.
   * PathGroup 이름 : PathGroup의 이름을 입력합니다.
   * PathGroup 유형 : [PathGroup의 유형](pathgroup.md#pathgroup)을 선택합니다.
   * Domain 이름 : PathGroup 유형에 맞게 Cisco ACI에 사전 정의된 Domain을 선택합니다
   * VLAN 범위 : VLAN Pool 범위내에서 사용할 VLAN 설정이 가능합니다. (default : VLAN Pool 전체)&#x20;
   * PathEndpoint 구성 : PathGroup으로 그룹화할 Path Endpoint 정보를 추가합니다\
     \* 목록에 등록된 PathEndpoint를 삭제하고자 할 경우, 휴지통 🗑 버튼을 클릭합니다.
   * 설명 : PathGroup에 대한 설명을 입력합니다.
4. 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (552).png" alt="" width="563"><figcaption></figcaption></figure>

5. PathGroup 목록에서 생성한 PathGroup 을 확인합니다.

### PathGroup 수정

PathGroup을 수정하는 기능입니다.

1. 메뉴에서 SDN 관리 > PathGroup을 클릭하여 PathGroup 목록을 조회합니다.
2. 수정하려는 PathGroup 을 선택한 후 상단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

3. PathGroup 수정에 필요한 정보를 입력합니다. [PathGroup 생성](pathgroup.md#pathgroup-2)을 참고해주십시오.
4. 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (1) (2).png" alt="" width="563"><figcaption></figcaption></figure>

5. PathGroup 목록에서 수정한 PathGroup 정보를 확인합니다.

### PathGroup 삭제

PathGroup 정보를 삭제하는 기능입니다. 단, PathGroup이 사용중인 경우 삭제가 불가능합니다.

1. 메뉴에서 SDN 관리 > PathGroup을 클릭하여 PathGroup 목록을 조회합니다.
2. 수정하려는 PathGroup 을 선택한 후, 상단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

3. 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (232).png" alt="" width="375"><figcaption></figcaption></figure>

4. PathGroup 목록에서 삭제한 PathGroup 을 확인합니다.

### PathGroup 수동 동기화

PathGroup의 PathEndpoint를 수정한 경우, 해당 PathGroup를 사용중인 기존 리소스에 PathGroup의 변경사항을 수동으로 반영할 수 있는 기능입니다.

동기화 상태가 "미완료"인 경우, 수동 동기화 버튼이 활성화됩니다.

1. 메뉴에서 SDN 관리 > PathGroup을 클릭하여 PathGroup 목록을 조회합니다.
2. 동기화가 필요한 PathGroup 을 선택한 후, 상단의 **\[수동 동기화]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

3. PathGroup 수동 동기화 팝업 창이 열리면, 반영할 Subnet을 선택한 다음 팝업 창 우측 하단의 **\[동기화]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (237).png" alt=""><figcaption></figcaption></figure>

4. PathGroup의 동기화 상태를 확인하여 동기화가 정상적으로 이루어졌는지 확인합니다.

## FAQ

> **Q. PathGroup 생성이 되지 않습니다.**
>
> A. [PathGroup 생성](pathgroup.md#pathgroup-1) 을 참고해주시기 바랍니다. PathGroup 생성 절차대로 진행했음에도 생성되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. PathGroup 삭제가 되지 않습니다.**
>
> A. [PathGroup 삭제](pathgroup.md#pathgroup-3) 를 참고해주시기 바랍니다. PathGroup 삭제 절차대로 진행했음에도 삭제되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
