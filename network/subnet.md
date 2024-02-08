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

# Subnet

***

## 개요

Subnet 은 [VPC](vpc.md) 내 세분화된 네트워크 영역으로, VPC IP 주소 범위 내 세분화된 주소를 갖습니다.

Subnet 은 독립된 네트워크 영역으로 같은 VPC 내 존재하더라도 기본적으로 통신이 불가능하여, VPC 내 Subnet 간 통신을 위해서 [Routing](routing.md) 설정이 필요합니다.

Tenant, VPC 에 대한 접근 권한이 있는 경우에만 하위에 Subnet 생성, 수정, 삭제가 가능합니다.

## 사용 가이드

### Subnet 목록 조회

메뉴에서 Network > Subnet 을 클릭하여 Subnet 목록을 조회합니다.&#x20;

<figure><img src="../.gitbook/assets/image (473).png" alt=""><figcaption></figcaption></figure>

### Subnet 생성

Subnet 생성은 VPC 내 Subnet 을 생성하는 기능입니다.

{% hint style="info" %}
참고

* VPC 내 Subnet 간 Subnet IP 주소는 서로 겹칠 수 없습니다.
* Subnet은 VPC 당 최대 3개 생성 가능합니다.
* Subnet 이름, VPC, Subnet 주소 정보는 수정이 불가능 합니다. 생성 입력 시 유의하시기 바랍니다.
* Subnet 생성 후 Subnet 주소는 '게이트웨이 IP/Bitmask' 형태로 전환됩니다.
  * 예시1) 192.168.0.10/24 -> 192.168.0.1/24
  * 예시2) 192.168.0.10/29 -> 192.168.0.9/29
{% endhint %}

1. 메뉴에서 Network > Subnet 을 선택합니다.
2. Subnet 목록 화면이 나타나면, 상단 메뉴 중 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (472).png" alt=""><figcaption></figcaption></figure>

3. Subnet 생성 팝업 창이 나타나면, Subnet 생성 정보를 입력합니다.
   * Subnet 이름 : Subnet 이름을 입력합니다.
   * VPC : Subnet이 생성될 대상 VPC를 선택합니다.
   * Subnet 주소 : 생성할 Subnet 의 IP 주소 범위를 입력합니다. 선택한 VPC의 IP 주소 범위 내에서 입력 가능하며, /8\~/29 범위여야 합니다.
   * 설명 : Subnet에 대한 상세 설명을 입력합니다.
4. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (474).png" alt="" width="375"><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 생성한 Subnet이 Subnet 목록 화면에 추가된 것을 확인합니다.

### Subnet 수정

Subnet 정보를 수정하는 기능으로, Subnet에 대한 설명만 수정 가능합니다.

1. 메뉴에서 Network > Subnet 을 선택합니다.
2. Subnet 목록 화면이 나타나면 수정하려는 Subnet을 선택한 다음, 상단 메뉴 중 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (475).png" alt=""><figcaption></figcaption></figure>

3. Subnet 수정 팝업 창이 나타나면, Subnet 정보를 수정합니다.
4. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (477).png" alt="" width="375"><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, Subnet 목록 화면에 수정 사항이 반영된 것을 확인합니다.

### Subnet 삭제

Subnet 삭제는 VPC 내 Subnet 을 삭제하는 기능입니다.

{% hint style="danger" %}
**주의**

* Subnet 하위에 Network Interface가 존재하지 않아야 삭제가 가능합니다.
* Subnet 삭제 시, Routing 정보(Routing, VPC Peering, Gateway 연결, Cloud Connect 연결)도 함께 삭제 됩니다.
{% endhint %}

1. 메뉴에서 Network > Subnet 을 선택합니다.
2. Subnet 목록 화면이 나타나면 삭제하려는 Subnet을 선택한 다음, 상단 메뉴 중 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (476).png" alt=""><figcaption></figcaption></figure>

3. Subnet 삭제를 위한 팝업 창이 나타나면, 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (478).png" alt="" width="375"><figcaption></figcaption></figure>

4. 삭제 팝업 창이 닫히고, Subnet 목록에서 Subnet이 삭제되었는지 확인합니다.

## FAQ

> **Q. Subnet 생성이 되지 않습니다.**
>
> A. [Subnet 생성](subnet.md#subnet) 을 참고해주시기 바랍니다. Subnet 생성 절차대로 진행했음에도 생성되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. Subnet 삭제가 되지 않습니다.**
>
> A. [Subnet 삭제](subnet.md#subnet-2) 를 참고해주시기 바랍니다. Subnet 삭 절차대로 진행했음에도 생성되지 않는다면  시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. Subnet 는 몇 개까지 생생 가능한가요?**
>
> A. Subnet 는 VPC 당 최대 3개 생성 가능합니다.
