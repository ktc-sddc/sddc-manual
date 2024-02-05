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





4. 방화벽 상품 선택

이중화 여부 / 방화벽 사양 등의 상품 정보를 고려하여, 네트워크 환경에 맞는 방화벽 상품을 선택한 후, **다음** 버튼을 클릭합니다

<figure><img src="../.gitbook/assets/image (665).png" alt=""><figcaption></figcaption></figure>

5. 기본정보 입력

방화벽 이름과 설명을 입력한 후 **생성** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (666).png" alt=""><figcaption></figcaption></figure>



###

## FAQ

> **Q. 정책의 순서를 변경하고 싶습니다.**
>
> A. 현재는 정책의 순서 변경 기능을 지원하지 않고 있습니다. 정책을 삭제하고, 생성하여 주시기 바랍니다.

> **Q. 정책이 생성/삭제가 되지 않습니다.**
>
> A. 시스템 관리자(sddc.ktcloud@kt.com)에게 문의하시기 바랍니다.
