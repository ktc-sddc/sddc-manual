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

# Colocation Gateway 관리(이미지 변경)

***

## 개요

SDDC Platform 사용자에게 제공되는 Colocation Gateway 상품에 대한 관리 기능을 제공합니다.

관리자를 통하여 사용자가 요청한 Tenant에 Colocation Gateway를 생성하고 삭제할 수 있습니다.

## 사용 가이드

### Colocation Gateway 신청 목록 조회

1. 메뉴에서 SDN 관리 > Colocation Gateway 관리를 클릭합니다.
2. **\[신청목록 관리]** 탭을 클릭합니다.
3. **\[미처리 내역]** 탭과 **\[전체]** 탭을 통하여 신청 목록을 조회 합니다.

이미지

### Colocation Gateway 신청 내역 처리

1. 신청자에게 개별 연락하여, Colocation Gateway 신청에 대한 상세 내용을 문의합니다.
2. 신청내역을 선택하고 **\[처리]** 버튼을 클릭하여, 승인/반려 처리를 합니다.

이미지

3. 승인 처리를 한 경우, 신청 내용을 바탕으로  [PathGroup](pathgroup.md) / [Gateway Info](gateway-info.md)를 생성합니다.
4. 다시 **\[처리]** 버튼을 클릭하여, Gateway를 생성합니다. 3번에서 생성한 Gateway Info를 선택하여 생성합니다.

이미지

5. **\[생성 내역 관리]** 탭을 클릭하여, 생성된 Colocation Gateway를 확인합니다.



### Colocation Gateway 전체 목록 조회

메뉴 SDN 관리 > Colocation Gateway 관리의 **\[생성 내역 관리]** 탭에서 전체 Colocation Gateway 목록을 조회합니다.

이미지

### Colocation Gateway 생성

Colocation Gateway를 생성하는 기능입니다.&#x20;

1. 메뉴 SDN 관리 > Colocation Gateway 관리의 **\[생성 내역 관리]** 탭에서, **\[생성]** 버튼을 클릭합니다.

이미지

2.  Colocation Gateway 생성 팝업 창이 나타나면, Colocation Gateway 생성 정보를 입력합니다.

    * Colocation Gateway 이름 : Colocation Gateway 이름을 입력합니다.
    * Gateway Info : Gateway 기준정보를 선택합니다.
    * Tenant 이름 : Colocation Gateway가 생성될 Tenant를 선택합니다.


3. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

생성 팝업 이미지

4. 팝업 창이 닫히고, 생성한 Colocation Gateway가 추가된 것을 확인합니다.

### Colocation Gateway 삭제

Tenant에 생성된 Colocation Gateway를 삭제하는 기능입니다.

{% hint style="danger" %}
**주의**

* Colocation Gateway 삭제 시, Subnet 연결 정보도 함께 삭제됩니다.
{% endhint %}

1. 메뉴 SDN 관리 > Colocation Gateway 관리의 **\[생성 내역 관리]** 탭에서, 삭제할 Colocation Gateway를 선택하고 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (252).png" alt=""><figcaption></figcaption></figure>

2. Colocation Gateway 삭제 팝업 창이 나타나면, 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (253).png" alt="" width="375"><figcaption></figcaption></figure>

3. 삭제 팝업 창이 닫히고, Colocation Gateway가 삭제되었는지 확인합니다.

## FAQ

> **Q. Colocation Gateway 생성이 되지 않습니다.**
>
> A. [Colocation Gateway 생성 ](colocation-gateway.md#gateway-1)참고해주시기 바랍니다. 만약 해결되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. Colocation Gateway 삭제가 되지 않습니다.**
>
> A. [Colocation Gateway 삭제](colocation-gateway.md#gateway-2)를 참고해주시기 바랍니다. 만약 해결되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
