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

<figure><img src="../../.gitbook/assets/image (617) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Cloud 상품 생성

사용자에게 제공할 Cloud 상품을 생성합니다.

{% hint style="info" %}
**참고**

* 사용 여부를 사용으로 설정해야 사용자에게 Cloud 상품이 노출됩니다.
{% endhint %}

1. 시스템 관리 > OpenStack 관리 > Cloud 상품 메뉴를 클릭합니다.
2. 화면 왼쪽 Cloud 상품 목록 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 3.00.18 2.png" alt=""><figcaption></figcaption></figure>

3. Cloud 상품 생성 창에서 관리대상, 상품 유형과 이름, 설명을 입력한 후 **\[다음]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (619).png" alt=""><figcaption></figcaption></figure>

4. Flavor, Volume, Share의 유형에 맞게 목록을 선택한 후, 생성 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (620).png" alt=""><figcaption></figcaption></figure>

### Cloud 상품 수정

Cloud 상품 사용 여부, 이름 수정, type 연동 기능을 제공합니다.

{% hint style="danger" %}
**주의**

* Type이 연결되지 않은 Cloud 상품은 반드시 미사용 상태로 변경해야 하며, 그렇지 않을 경우 Volume 생성 시 오류가 발생할 수 있습니다.
{% endhint %}

1. 시스템 관리 > OpenStack 관리 > Cloud 상품 메뉴를 클릭합니다.
2. 화면 왼쪽 Cloud 상품 목록 상단에 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 3.00.18 3.png" alt=""><figcaption></figcaption></figure>

3. Cloud 상품 수정 창에서 수정할 정보를 입력한 후 **\[다음]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (622).png" alt=""><figcaption></figcaption></figure>

4. 필요한 정보를 수정한 이후, 수정 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (623).png" alt=""><figcaption></figcaption></figure>

### Cloud 상품 삭제

사용하지 않는 Cloud 상품을 삭제합니다.

1. 시스템 관리 > OpenStack 관리 > Cloud 상품 관리 메뉴를 클릭합니다.
2. 삭제할 Cloud 상품을 선택하고 목록 상단에 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 3.00.18.png" alt=""><figcaption></figcaption></figure>

3. 삭제 팝업 창에서 삭제할 대상을 확인 후 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (625).png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. Cloud 상품을 삭제하려면, 어떻게 해야하나요?**
>
> **A. 해당 상품에 연결된 유형(Flavor, VolumeType, ShareType) 을 관리 대상 제외하고 삭제 하셔야 합니다.**
