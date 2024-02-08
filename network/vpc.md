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

# VPC

***

## 개요

VPC(Virtual Private Cloud)는 논리적으로 격리된 가상의 네트워크에서 SDDC Platform 리소스를 운영할 수 있는 기능을 제공합니다.

* VPC는 Tenant 하위에 생성되며, Tenant 당 최대 3개까지 생성 가능합니다.
* 동일한 Tenant 내 VPC 간 통신을 하기 위해선 [VPC Peering](vpc-peering.md) 이 필요합니다.
* VPC 하위에 독립된 네트워크인 [Subnet](subnet.md)을 생성하여 IT 인프라를 안전하게 구축하고 간편하게 관리할 수 있습니다.
* Tenant 접근 권한이 있는 경우에만 VPC 생성, 수정, 삭제가 가능합니다.

#### VPC IP 주소 범위

VPC의 IP 주소범위는 IPv4 CIDR 형식이며, RFC 1918에 명시되어 있는 3개의 표준 Private IP 대역을 따릅니다.

<table><thead><tr><th width="159.58080556936847">RFC1918</th><th width="164">CIDR</th><th width="127.33333333333331">Prefix</th><th>IP 주소 범위</th></tr></thead><tbody><tr><td>24-bit block</td><td>10.0.0.0/8</td><td>10/8</td><td>10.0.0.0~10.255.255.255</td></tr><tr><td>20-bit block</td><td>172.16.0.0/12</td><td>172.16/12</td><td>172.16.0.0~172.31.255.255</td></tr><tr><td>16-bit block</td><td>192.168.0.0/16</td><td>192.168/16</td><td>192.168.0.0~192.168.255.255</td></tr></tbody></table>

{% hint style="info" %}
**참고**

VPC IP 주소범위는 Cloud 운영 정책에 의해 변경 될 수 있습니다.

VPC 최대 생성 개수는 [Quota](../management-new/quota.md) 기능을 통해 변경 할 수 있습니다.
{% endhint %}

## 사용 가이드

### VPC 목록 조회

메뉴에서 Network > VPC 를 클릭하여 VPC 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (707).png" alt=""><figcaption></figcaption></figure>

### VPC 생성

{% hint style="info" %}
참고

* Tenant 내 VPC 간 IP 주소 범위(CIDR)는 겹칠 수 없습니다.
* VPC 는 Tenant 당 최대 3개 생성 가능합니다.
* VPC 이름, IP 주소 범위(CIDR)는 수정이 불가능합니다. 생성 입력 시 유의하시기 바랍니다.
* VPC 생성 후 VPC주소는 'Network 이름/Bitmask' 형태로 전환됩니다.
  * 예시1) 192.168.0.10/24 -> 192.168.0.0/24
  * 예시2) 192.168.0.10/29 -> 192.168.0.8/29
{% endhint %}

1. 메뉴에서 Network > VPC 를 선택합니다.
2. VPC 목록 화면이 나타나면, 상단 메뉴 중 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (708).png" alt=""><figcaption></figcaption></figure>

3. VPC 생성 팝업 창이 나타나면, VPC 생성 정보를 입력합니다.
   * VPC 이름 : VPC 이름을 입력합니다.
   * IP 주소 범위(CIDR) : 팝업 상단의 입력 가능한 IP 주소범위(CIDR) 가이드를 참고하여, VPC의 IP 주소범위를 입력합니다.
   * 설명 : 상세 설명을 입력합니다
4. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (715).png" alt="" width="453"><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 생성한 VPC가 VPC 목록 화면에 추가된 것을 확인합니다.

### VPC 수정

1. 메뉴에서 Network > VPC 를 선택합니다.
2. VPC 목록 화면이 나타나면 수정하려는 VPC를 선택한 다음, 상단 메뉴 중 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (709).png" alt=""><figcaption></figcaption></figure>

3. VPC 수정 팝업 창이 나타나면, VPC 정보를 수정합니다.
4. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (714).png" alt="" width="453"><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, VPC 목록 화면에 수정 사항이 반영된 것을 확인합니다.

### VPC 삭제

{% hint style="danger" %}
**주의**

* VPC 삭제 시, VPC에 연결된 VPC Peering 정보도 함께 삭제됩니다.
* VPC 하위에 Subnet이 존재하지 않아야 VPC 삭제가 가능합니다.
{% endhint %}

1. 메뉴에서 Network > VPC를 선택합니다.
2. VPC 목록 화면이 나타나면 삭제하려는 VPC를 선택한 다음, 상단 메뉴 중 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (711).png" alt=""><figcaption></figcaption></figure>

3. VPC 삭제를 위한 팝업 창이 나타나면, 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (713).png" alt="" width="336"><figcaption></figcaption></figure>

4. 삭제 팝업 창이 닫히고, VPC 목록에서 VPC가 삭제되었는지 확인합니다.

## FAQ

> **Q. VPC 생성이 되지 않습니다.**
>
> A. [VPC 생성](vpc.md#vpc)을 참고해주시기 바랍니다. 만약 해결 되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. VPC 삭제가 되지 않습니다.**
>
> A. [VPC 삭제](vpc.md#vpc-2)를 참고해주시기 바랍니다. 만약 해결 되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. VPC 는 몇 개까지 생성 가능한가요?**
>
> A. VPC 는 Tenant 당 최대 3개 생성 가능합니다.
