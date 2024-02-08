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

# VPC Peering

***

## 개요

VPC Peering 은 동일 Tenant 내 다른 VPC 하위의 Subnet 간 통신을 위한 기능입니다.

[VPC](vpc.md)는 독립된 네트워크 공간으로 동일한 Tenant 내 존재하더라도 서로 통신이 불가능하지만, VPC Peering 을 통해 통신이 가능하게 됩니다.

## 사용 가이드

### VPC Peering 목록 조회

Tenant 내 전체 VPC Peering 목록을 조회하는 기능입니다.

1. 메뉴에서 Network > VPC Peering 을 클릭하여 VPC Peering 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

### VPC Peering 생성

VPC Peering 생성은 서로 다른 VPC 내 Subnet 사이에 통신 관계를 생성하는 기능입니다.

{% hint style="info" %}
참고

* 이미 VPC Peering 이 생성된 VPC 간에는 VPC Peering 을 생성할 수 없습니다.
{% endhint %}

1. 메뉴에서 Network > VPC Peering 을 클릭하여 VPC Peering 목록을 조회합니다.
2. 상단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

3. VPC Peering 생성 정보를 입력합니다.
   * VPC Peering 이름 : 생성될 VPC Peering 의 이름입니다.
   * VPC 1 : VPC Peering 통신을 할 VPC 입니다. VPC 선택 후 하위 Subnet 을 선택할 수 있으며, 복수 개 선택이 가능합니다. 선택한 Subnet은 Routing Table 에 등록됩니다.
   * VPC 2 : VPC Peering 통신을 할 VPC 입니다. VPC 선택 후 하위 Subnet 을 선택할 수 있으며, 복수 개 선택이 가능합니다. 선택한 Subnet은 Routing Table 에 등록됩니다.
   * 설명 : VPC Peering 에 대한 상세한 설명입니다.
4. 팝업창 우측 하단 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (27).png" alt="" width="375"><figcaption></figcaption></figure>

5. VPC Peering 목록에서 생성한 VPC Peering 을 확인합니다.

### VPC Peering 수정

VPC Peering 정보를 수정하는 기능입니다. VPC Peering 설명을 수정할 수 있습니다.

1. 메뉴에서 Network > VPC Peering 를 클릭하여 VPC Peering 목록을 조회합니다.
2. 수정할 VPC Peering 선택 후, 상단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

3. VPC Peering 수정 정보를 입력합니다.
4. 팝업창 우측 하단 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (3).png" alt="" width="453"><figcaption></figcaption></figure>

5. VPC Peering 목록에서 수정한 VPC Peering 의 수정 사항을 확인합니다.

### Peering 관리

VPC Peering 내에 연결할 Subnet 목록을 추가/삭제 할 수 있습니다.

1. 메뉴에서 Network > VPC Peering를 클릭하여 VPC Peering 목록을 조회합니다.
2. Peering 연결목록을 관리할 VPC Peering 선택 후, 상단의 **\[Peering 관리]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

3. Peering 내 VPC1 의 Peering 대상 Subnet 목록을 수정합니다.
   * Subnet 추가 : Subnet을 선택 후, **\[추가]** 버튼을 클릭합니다.
   * Subnet 삭제 : 삭제할 Subnet 우측 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image.png" alt="" width="453"><figcaption></figcaption></figure>

4. Peering 내 VPC2 의 Peering 대상 Subnet 목록을 수정합니다.
   * Subnet 추가 : Subnet을 선택 후, **\[추가]** 버튼을 클릭합니다.
   * Subnet 삭제 : 삭제할 Subnet 우측 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (1).png" alt="" width="453"><figcaption></figcaption></figure>

5. Peering 관리 팝업에서 Routing 대상 Subnet 목록 수정 사항을 확인합니다.

### VPC Peering 삭제

VPC Peering 정보를 삭제하는 기능입니다.

1. 메뉴에서 Network > VPC Peering를 클릭하여 VPC Peering 목록을 조회합니다.
2. 삭제할 VPC Peering 선택 후, 상단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (716).png" alt=""><figcaption></figcaption></figure>

3. 팝업창 우측 하단 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (2).png" alt="" width="336"><figcaption></figcaption></figure>

4. VPC Peering 목록에서 VPC Peering 삭제 여부를 확인합니다.

## FAQ

> **Q. VPC Peering에 NFV Device 를 연결하고 싶습니다.**
>
> **A.** 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
