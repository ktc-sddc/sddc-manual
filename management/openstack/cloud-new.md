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

# Cloud 상품 관리(new)

## 개요

SDDC Platform 사용자에게 제공되는 상품에 대한 관리 기능을 제공합니다.

플랫폼에서 제공하는 Server, Volume, Share 의 상품을 정의하고 연동합니다.

## 사용 가이드

### Cloud 상품 목록 조회

사용자에게 제공하는 Cloud 상품 목록을 조회합니다.

1. 시스템 관리 > OpenStack 관리 > Cloud 상품 관리 메뉴를 클릭합니다.
2. 화면 왼쪽 Cloud 상품 목록 정보를 확인합니다.
   * 사용: 사용자들에게 제공 여부를 결정합니다.

<figure><img src="../../.gitbook/assets/image (336).png" alt=""><figcaption></figcaption></figure>

### Cloud 상품 생성

사용자에게 제공할 Cloud 상품을 생성합니다.

{% hint style="info" %}
**참고**

* 사용 여부를 사용으로 설정해야 사용자에게 Cloud 상품이 노출됩니다.
{% endhint %}

1. 시스템 관리 > OpenStack 관리 > Cloud 상품 메뉴를 클릭합니다.
2. 화면 왼쪽 Cloud 상품 목록 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (337).png" alt=""><figcaption></figcaption></figure>

3. Cloud 상품 생성 팝업 창에서 정보를 입력한 후 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (338).png" alt=""><figcaption></figcaption></figure>

### Cloud 상품 수정

Cloud 상품 사용 여부, 이름 수정, type 연동 기능을 제공합니다.

{% hint style="danger" %}
**주의**

* Type이 연결되지 않은 Cloud 상품은 반드시 미사용 상태로 변경해야 하며, 그렇지 않을 경우 Volume 생성 시 오류가 발생할 수 있습니다.
{% endhint %}

1. 시스템 관리 > OpenStack 관리 > Cloud 상품 메뉴를 클릭합니다.
2. 화면 왼쪽 Cloud 상품 목록 상단에 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (313).png" alt=""><figcaption></figcaption></figure>

3. Cloud 상품 수정 팝업 창에서 정보를 입력한 후 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (318).png" alt=""><figcaption></figcaption></figure>

### Cloud 상품 삭제

사용하지 않는 Cloud 상품을 삭제합니다.

{% hint style="danger" %}
**주의**

* Type을 삭제할 경우, 기존 생성된 Volume에서 상품 정보가 노출되지 않습니다.
* Type을 삭제할 경우 연결된 OpenStack Type의 연결이 해제됩니다.
{% endhint %}

1. 시스템 관리 > OpenStack 관리 > Cloud 상품 관리 메뉴를 클릭합니다.
2. 삭제할 Cloud 상품을 선택하고 목록 상단에 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (314).png" alt=""><figcaption></figcaption></figure>

3. 삭제 팝업 창에서 삭제할 대상을 확인 후 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (319).png" alt="" width="375"><figcaption></figcaption></figure>

## FAQ

> **Q. Volume Product에 여러 개의 Volume Type이 연결되어있을 경우, Volume 생성 시 어떤 Type으로 생성되나요?**
>
> **A.** 연결 목록에서 첫 번째 Volume Type으로 Volume이 생성됩니다. 따라서 원하는 Volume Type으로 생성될 수 있도록 목록에서 사용하지 않는 Volume Type은 관리 대상에서 제외해야 합니다.

> **Q. 동일한 Volume Type이 A -> B Volume Product로 연결 정보가 변경될 경우, 해당 Volume Type을 사용하는 Volume의 Product Type은 어떻게 되나요?**
>
> **A.** 변경된 Volume Product 정보로 제공됩니다.
