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

# Internet Gateway

***

## 개요

Internet Gateway를 통해 Internet 연결 서비스를 제공합니다. Internet Gateway에 Subnet을 연결하여 Internet 을 사용 할 수 있습니다. Tenant에 1개의 Internet Gateway를 생성할 수 있습니다.

{% hint style="info" %}
참고

Tenant 당 1개의 Internet Gateway를 생성할 수 있습니다.
{% endhint %}

## 사용가이드

### Internet Gateway **생성**

Internet Gateway 를 생성하는 기능입니다.

1. 메뉴에서 Network > Internet Gateway 에서 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (557).png" alt=""><figcaption></figcaption></figure>

2. Internet Gateway 이름을 입력하고, **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (558).png" alt="" width="336"><figcaption></figcaption></figure>

3. 생성 목록을 확인합니다.

### Internet Gateway 목록 조회

Internet Gateway를 조회하는 기능입니다.

1. 메뉴에서 Network > Internet Gateway 에서 Internet Gateway 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (555).png" alt=""><figcaption></figcaption></figure>

### Internet Gateway 연결 관리

Internet Gateway에 Subnet 연결을 추가/삭제 할 수 있습니다.

1. Subnet 연결 관리할 Internet Gateway를 선택하여, **\[Subnet 연결 관리]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (554).png" alt=""><figcaption></figcaption></figure>

2. 연결된 Subnet 목록을 수정합니다.
   * Subnet 추가 : Subnet을 선택 후, **\[추가]** 버튼을 클릭합니다.
   * Subnet 삭제 : 삭제할 Subnet 우측 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (556).png" alt="" width="453"><figcaption></figcaption></figure>

3. 연결된 Subnet 목록을 확인합니다.

### Internet Gateway 삭제

Internet Gateway를 삭제하는 기능입니다.

1. 삭제할 Internet Gateway 선택 후, 상단의 **\[삭제]** 버튼을 클릭합니다.

{% hint style="warning" %}
주의

연결된 Subnet이 있는 경우, Internet Gateway 삭제 할 수 없습니다.
{% endhint %}

<figure><img src="../.gitbook/assets/image (553).png" alt=""><figcaption></figcaption></figure>

2. 팝업창 우측 하단 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (552) (1).png" alt="" width="386"><figcaption></figcaption></figure>

3. Internet Gateway 목록에서 삭제 여부를 확인합니다.

