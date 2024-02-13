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

# Shared Colocation Gateway 관리

***

## 개요

Shared Colocation Gateway는 다수의 Tenant 가 공용으로 사용 가능한 [Colocation Gateway](../network/colocation-gateway-routing.md)입니다. \
Shared Colocation Gateway 생성/삭제하고, 사용 신청을 처리 및 연결된 Tenant 를 관리합니다.

#### Member Tenant

Member Tenant 는 Shared Colocation Gateway 사용 권한을 갖은 Tenant 를 의미합니다. Member Tenant 는 관리자가 직접 추가하거나 삭제하는 것 외에도 사용 신청 관리 를 통해 사용 권한을 부여할 수 있습니다.&#x20;

Member 로 등록된 Tenant 는  [Shared Colocation Gateway](cloud-connect.md) 메뉴를 통해 사용 권한을 갖은 Shared Colocation Gateway 를 조회할 수 있으며, Subnet을 연결 할 수 있습니다.



## 사용 가이드

### Shared Colocation Gateway 사용 신청 목록 조회

전체 Shared Colocation Gateway 사용 신청 내역을 조회하는 기능입니다.

1. 메뉴 SDN 관리 > Shared Colocation Gateway 관리 **\[신청 목록 관리]** 탭에서 사용 신청 내역을 조회합니다. 신청 내역은 미처리 내역과 처리 완료 내역으로 구분됩니다.

<figure><img src="../.gitbook/assets/image (572).png" alt=""><figcaption></figcaption></figure>

### Shared Colocation Gateway 사용 신청 승인

Shared Colocation Gateway 사용 신청을 승인하는 기능입니다. 승인 메시지를 작성하여 요청자에게 전달할 수 있으며, 승인된 Tenant 는 Shared Colocation Gateway 의 Member Tenant로 등록되며 사용 권한을 갖게 됩니다.

1. 메뉴 SDN 관리 > Shared Colocation Gateway 관리 **\[신청 목록 관리]** 탭에서, 신청 내역서의 **\[처리]** 버튼을 클랙합니다.

<figure><img src="../.gitbook/assets/image (573).png" alt=""><figcaption></figcaption></figure>

2. 승인을 선택하고, 메시지를 입력합니다.

<figure><img src="../.gitbook/assets/image (576).png" alt="" width="453"><figcaption></figcaption></figure>

3. 처리 완료 내역에서 승인한 신청이 조회 되는지 확인합니다.

### Shared Colocation Gateway 사용 신청 반려

Shared Colocation Gateway 사용 신청을 반려하는 기능입니다. 반려 메시지를 작성하여 요청자에게 전달할 수 있습니다.

1. 메뉴 SDN 관리 > Shared Colocation Gateway 관리 **\[신청 목록 관리]** 탭에서, 신청 내역서의  **\[처리]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (574).png" alt=""><figcaption></figcaption></figure>

2. 반려를 선택하고, 메시지를 입력합니다.

<figure><img src="../.gitbook/assets/image (577).png" alt="" width="453"><figcaption></figcaption></figure>

3. 처리 완료 내역에서 반려한 신청이 조회 되는지 확인합니다.

### Shared Colocation Gateway 목록 조회

전체 Shared Colocation Gateway 목록을 조회하는 기능입니다.

메뉴 SDN 관리 > Shared Colocation Gateway 관리 **\[생성 내역 관리]** 탭을 클릭하여 Shared Colocation Gateway 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (578).png" alt=""><figcaption></figcaption></figure>

### Shared Colocation Gateway 생성

Shared Colocation Gateway 를 생성하는 기능입니다. 생성한 Shared Colocation Gateway는 사용 가능한 Shared Colocation Gateway 목록에서 조회될 수 있습니다.

1. 메뉴 SDN 관리 > Shared Colocation Gateway 관리 **\[생성 내역 관리]** 탭에서 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (579).png" alt=""><figcaption></figcaption></figure>

2.  Shared Colocation Gateway  생성 정보를 입력합니다.

    1. Shared Colocation Gateway 이름: 생성할 Shared Colocation Gateway 이름입니다.
    2. Gateway Info: 사용할 Gateway Info 정보 입니다.
    3. System Tenant: Shared Colocation Gateway 가 생성될 System Tenant 입니다.

    <figure><img src="../.gitbook/assets/image (584).png" alt="" width="453"><figcaption></figcaption></figure>
3. **\[생성]** 버튼을 클릭합니다.
4. Shared Colocation Gateway 목록에서 생성 되었는지 확인합니다.

### Member Tenant 추가

Tenant 를 Shared Colocation Gateway 의 Member Tenant 로 등록하여 Shared Colocation Gateway 사용 권한을 부여하는 기능입니다.

1. 메뉴 SDN 관리 > Shared Colocation Gateway 관리 **\[생성 내역 관리]** 탭에서 **\[Tenant 등록 관리]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (580).png" alt=""><figcaption></figcaption></figure>

2. 등록된 Tenant 목록 하위 Tenant 선택 목록에서 Member 로 추가할 Tenant 를 선택 후 **\[추가]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (586).png" alt="" width="453"><figcaption></figcaption></figure>

3. 등록된 Tenant 목록에서 추가 되었는지 확인합니다.

### Member Tenant 회수

Tenant를 Shared Colocation Gateway의 Member Tenant 에서 제거하여 Shared Colocation Gateway 사용 권한을 회수하는 기능입니다.

{% hint style="info" %}
**참고.**

[Tenant 등록 관리](cloud-connect.md#3.-member-tenant) 를 통해 사용 권한이 회수 되면 기존의 승인된 요청이 회수 상태로 전환됩니다.
{% endhint %}

1. 메뉴 SDN 관리 > Shared Colocation Gateway 관리 **\[생성 내역 관리]** 탭에서 **\[Tenant 등록 관리]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (581).png" alt=""><figcaption></figcaption></figure>

2. 등록된 Tenant 목록에서 권한을 회수할 Tenant 를 선택 후 회수 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (587).png" alt="" width="453"><figcaption></figcaption></figure>

3. 사용 권한 회수 팝업 창이 나타나면, 회수할 Tenant 정보를 확인한 다음 팝업 창 우측 하단의 **\[회수]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (588).png" alt="" width="453"><figcaption></figcaption></figure>

4. 회수 처리가 완료되면, Member Tenant 목록에서 회수한 Tenant가 삭제 되었는지 확인합니다.
5. 메뉴 SDN 관리 > Shared Colocation Gateway 관리 **\[신청 목록 관리]** / **\[전체]** 탭에서 해당 신청 내역의 처리 상태가 "회수 처리" 상태로 변경 되었는지 확인합니다.(신청을 통해 사용 권한을 획득한 경우)

<figure><img src="../.gitbook/assets/image (589).png" alt=""><figcaption></figcaption></figure>

### Shared Colocation Gateway 삭제

Shared Colocation Gateway 를 삭제하는 기능입니다.

{% hint style="warning" %}
**주의**

연결된 Subnet이 있는 경우, Shared Colocation Gateway 삭제 할 수 없습니다.
{% endhint %}

1. 메뉴 SDN 관리 > Shared Colocation Gateway 관리 **\[생성 내역 관리]** 탭에서 Shared Colocation Gateway 를 선택하고 좌측 상단의 **\[삭제]**버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (582).png" alt=""><figcaption></figcaption></figure>

2. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (265).png" alt="" width="375"><figcaption></figcaption></figure>

3. Shared Colocation Gateway 목록에서 삭제 되었는지 확인합니다.

## FAQ

> **Q. Shared Colocation Gateway 삭제 시, Member Tenant 정보는 어떻게 되나요?**
>
> A. Shared Colocation Gateway의 Member Tenant 정보는 모두 삭제됩니다.

> **Q. Shared Colocation Gateway 삭제 시, Subnet 연결 정보는 어떻게 되나요?**
>
> A. Shared Colocation Gateway에 연결된 Subnet 연결 정보는 모두 삭제됩니다.
