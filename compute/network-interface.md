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

# Network Interface

***

## 개요

Network Interface는 Server가 Subnet을 통해 내/외부로 통신할 수 있는 인터페이스입니다.\
뿐만 아니라 Network Interface에 Security Group을 적용하여 네트워크 트래픽에 대한 접근 제어 기능도 제공합니다.

#### DHCP Network Interface

Subnet 내에서 DHCP Agent와 통신하는 역할을 수행하는 Network Interface입니다. DHCP 프로토콜을 이용하여 IP를 자동 할당하기 위해 Subnet 생성 시 자동으로 생성됩니다.\
DHCP Network Interface는 수정 및 삭제가 불가능하며, Subnet을 삭제하면 함께 삭제됩니다.

## 사용 가이드

### Network Interface 목록 조회

1. Compute > Network Interface 버튼을 클릭합니다.
2. Network Interface 목록을 확인합니다.

<figure><img src="../.gitbook/assets/image (1) (1) (2).png" alt=""><figcaption></figcaption></figure>

### Network Interface 생성

1. Compute > Network Interface 버튼을 클릭합니다.
2. 목록 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-05 오후 2.05.04.png" alt=""><figcaption></figcaption></figure>

3. 생성 팝업 창에서 VM이 사용할 Network 정보를 입력하고 **\[생성]** 버튼을 클릭합니다.

* DHCP 사용/미사용 설정은 고정 IP 할당 여부를 결정합니다.
  * DHCP 사용: 자동으로 고정 IP를 할당합니다.
  * DHCP 미사용:사용자가 고정 IP를 지정하여 생성합니다.

<figure><img src="../.gitbook/assets/image (417).png" alt="" width="375"><figcaption></figcaption></figure>

### Network Interface 삭제

{% hint style="info" %}
**참고**

* Server에 적용되어 있는 Network Interface는 삭제가 불가능합니다.
* DHCP Network Interface는 삭제가 불가능하며, Subnet 삭제 시 함께 삭제됩니다.
{% endhint %}

1. Compute > Network Interface 버튼을 클릭합니다.
2. 목록에서 삭제할 대상을 선택하고 상단에 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-05 오후 2.05.04 3.png" alt=""><figcaption></figcaption></figure>

3. 삭제 팝업 창에서 대상을 확인하고 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (419).png" alt="" width="375"><figcaption></figcaption></figure>

### Network Interface의 Security Group 적용

1. Compute > Network Interface 버튼을 클릭합니다.
2. Security Group을 적용할 Network Interface를 선택 후 상단에 **\[SECURITY GROUP 수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-05 오후 2.06.47.png" alt=""><figcaption></figcaption></figure>

3. SECURITY GROUP 적용 팝업 창에서 수정 사항을 입력하고 **\[저장]** 버튼을 클릭합니다.\
   Network Interface마다 최대 3개의 Security Group을 적용할 수 있습니다.

<figure><img src="../.gitbook/assets/image (421).png" alt=""><figcaption></figcaption></figure>

### Network Interface 동기화

해당 Tenant 내의, 모든 Network Interface에 대해서 동기화 작업을 진행합니다.

비동기로 동작하여 바로 반영되지 않을 수 도 있습니다.

사용자는 사용자가 직접 생성하지 않고, 내부적으로 생성된 Network Interface에 대해서 제어 권한이 없습니다.

내부적으로 생성된 Network Interface에 대한 제어를 동기화 기능으로 제공됩니다.

1. 동기화 버튼 클릭

<figure><img src="../.gitbook/assets/스크린샷 2024-02-05 오후 2.10.13.png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. Network Interface에 Security Group은 몇 개 까지 적용이 가능한가요??**
>
> **A.** Network Interface에 최대 3개 까지 Security Group 적용이 가능합니다.
