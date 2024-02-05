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

# 방화벽

***

## 개요

방화벽 서비스는 Tenant 내에서 사용하는 자원을 보호하기 위해 제공하는 네트워크 보안 서비스입니다.

사용자의 Tenant 내 네트워크 트래픽 구성에 맞는 다양한 유형의 방화벽 서비스를 제공합니다.





## 사용가이드

### 방화벽 생성

1. Security > 방화벽 으로 이동합니다.
2. \[방화벽 생성] 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (663).png" alt=""><figcaption></figcaption></figure>

3. 방화벽 유형을 선택한 후 **다음** 버튼을 클릭합니다

{% hint style="warning" %}
방화벽을 적용하고자 하는 연결구간을 고려하여 방화벽을 생성해야 합니다.

* VPC Peering 구간 : Inner FW&#x20;
* Gateway routing 구간 : Outer FW
{% endhint %}

<figure><img src="../.gitbook/assets/image (664).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="136">구분</th><th width="482">설명</th><th>적용 가능 서비스</th></tr></thead><tbody><tr><td>Inner FW</td><td><p>하나의 Tenant 내부 연결 구간에 사용할 수 있는 방화벽 유형입니다.</p><p>one-arm 타입의 방화벽으로, east-west 트래픽 제어에 용이합니다.</p></td><td>VPC Peering</td></tr><tr><td>Outer FW</td><td>Tenant와 Tenant 외부 사이의 연결 구간에 사용할 수 있는 방화벽 유형입니다. two-arm 타입의 방화벽으로, north-south 트래픽 제어에 용이합니다.</td><td><p>Internet Gateway, </p><p>Colocation Gateway</p></td></tr></tbody></table>





4. 이중화 여부 / 방화벽 사양 등의 상품 정보를 고려하여, 네트워크 환경에 맞는 방화벽 상품을 선택한 후, **다음** 버튼을 클릭합니다

<figure><img src="../.gitbook/assets/image (665).png" alt=""><figcaption></figcaption></figure>

5. 방화벽 이름과 설명을 입력한 후 **생성** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (666).png" alt=""><figcaption></figcaption></figure>

6. 방화벽 메뉴에서 생성된 방화벽 상품을 확인합니다

<figure><img src="../.gitbook/assets/image (667).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
방화벽 상태가 **비정상** 인 경우 시스템 관리자(sddc.ktcloud@kt.com)에게 문의하시기 바랍니다.
{% endhint %}





### 방화벽 연결 생성



{% hint style="info" %}
방화벽 연결 생성을 위해서는 방화벽을 적용할 라우팅 정보를 미리 생성해야 합니다.

예를 들어, Inner FW의 경우 VPC Peering 리소스가 필요하고,  Outer FW의 경우 Internet(또는 Colocation) Gateway 연결 리소스가 필요합니다.

라우팅 연결 방법은 다음의 매뉴얼을 참고하시기 바랍니다.\
\- VPC Peering : Network > Routing \
\- Internet Gateway : Network > Internet Gateway\
\- Colocation Gateway : Network > Colocation Gateway
{% endhint %}



1. **방화벽 연결** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (668).png" alt=""><figcaption></figcaption></figure>

2. 방화벽 연결 생성 메뉴에서 필요 정보를 입력합니다.

* Inner FW\
  &#x20;\-  Target VPC 선택 : 방화벽이 생성될 Target VPC 를 선택합니다.  Target VPC와 VPC Peering으로 연결된 VPC 구간에는 "라우팅 리소스 추가"를 통해 방화벽 정책을 쉽게 적용할 수 있습니다.\
  &#x20;\-  라우팅 리소스 선택 : 방화벽이 적용될 VPC Peering 구간을 선택합니다.

<figure><img src="../.gitbook/assets/image (669).png" alt=""><figcaption></figcaption></figure>

* Outer FW





>
