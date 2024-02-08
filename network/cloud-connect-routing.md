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

# Shared Colocation Gateway

***

## 개요

Shared Colocation Gateway는 멀티 Tenant에서 사용 가능한 Colocation Gateway 서비스 입니다. Shared Colocation Gateway 사용 승인을 받아야 사용이 가능합니다.

{% hint style="warning" %}
주의

Shared Colocation Gateway에 연결 하는 Subnet 주소 범위는 서로 달라야 합니다.&#x20;
{% endhint %}

## 사용 가이드

### Shared Colocation Gateway 사용 신청

Tenant 내에서 Shared Colocation Gateway 를 사용하기 위해 신청하는 기능입니다.\
이미 사용 승인을 받았거나 사용 신청 처리중인 Cloud Connect 에 대한 사용 신청은 불가능합니다.

1. 메뉴에서 Network > Shared Colocation Gateway 에서  **\[서비스 신청]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

2. 서비스 신청 정보를 입력합니다.
3. 팝업창 우측 하단의 **\[신청]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1).png" alt="" width="453"><figcaption></figcaption></figure>

4. **\[신청 내역]** 탭을 클릭하여, 신청 내역이 조회 되는지 확인합니다.

### Shared Colocation Gateway 사용 신청 취소

Tenant 내에서 Shared Colocation Gateway 를 사용하기 위한 신청 내역을 취소하는 기능입니다.&#x20;

처리중 상태의 신청만 취소가 가능합니다.

1. 메뉴에서 Network > Shared Colocation Gateway 에서  **\[신청 내역]** 탭을 클릭하여, 신청 내역을 조횝 합니다.
2. 취소할 신청 내역을 선택하여, **\[신청 취소]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. 팝업창 우측 하단의 **\[확인]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (6) (1) (1).png" alt="" width="336"><figcaption></figcaption></figure>

4. 신청 내역에서 취소 처리가 되었는지 확인합니다.

### Shared Colocation Gateway 목록 조회

Tenant 내 전체 Shared Colocation Gateway 연결을 조회하는 기능입니다.

1. 메뉴에서 Network > Shared Colocation Gateway 을 클릭하여 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (7) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Shared Colocation Gateway 연결 관리

Shared Colocation Gateway 연결된 Subnet 목록을 추가/삭제 할 수 있습니다.

1. Subnet 연결 관리할 Shared Colocation Gateway을 선택 후, 상단의 **\[Subnet 연결 관리]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (8) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. 연결된 Subnet 목록을 수정합니다.
   * Subnet 추가 : Subnet을 선택 후, **\[추가]** 버튼을 클릭합니다.
   * Subnet 삭제 : 삭제할 Subnet 우측 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (9) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

4. 연결된 Subnet 목록을확인합니다.

## FAQ

> **Q. Shared Colocation Gateway 에 방화벽을 연결하고 싶습니다.**
>
> A. [Security > 방화벽](../nfv/firewall.md) 사용 가이드를 확인하시기 바랍니다.
>
>
>
> **Q. 사용 신청이 처리중 상태에서 진행되지 않습니다.**
>
> **A.** 사용 신청 검토는 영업일 기준 최대 7일이 소요될 수 있습니다. 만약 해결 되지 않는다면 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
>
>
>
> **Q. Shared Colocation Gateway를 생성하고 싶습니다.**
>
> **A.** 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

