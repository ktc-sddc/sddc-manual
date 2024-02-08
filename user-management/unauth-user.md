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

# 미승인 사용자 관리

***

## 개요

플랫폼에서 생성한 일반 사용자와 플랫폼 사용을 신청한 LDAP 사용자에게 ROLE을 부여하여 플랫폼 사용을 승인합니다. ROLE이 부여된 사용자는 플랫폼 접근이 가능해집니다.

## 사용자 가이드

#### 목록 조회

1. 사용자 관리 > 미승인 사용자 관리를 클릭합니다.
2. 미승인 사용자 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (520).png" alt=""><figcaption></figcaption></figure>

#### ROLE 관리

ROLE이 부여되지 않은 사용자에게 ROLE을 부여하여 플랫폼 접근을 승인합니다.

{% hint style="warning" %}
**참고**

승인 이후, 사용자는 승인 여부를 알 수 없기 때문에 별도로 승인 되었음을 안내해주시기를 바랍니다.
{% endhint %}

{% hint style="info" %}
**참고**

ROLE을 부여하는 관리자는 본인의 상위 ROLE을 부여할 수 없습니다.\
예) 관리자(ROLE\_ADMIN)가 시스템 관리자(ROLE\_SYSTEM\_ADMIN) ROLE 부여 불가능.
{% endhint %}

1. 사용자 관리 > 미승인 사용자 관리 메뉴를 클릭합니다.
2.  화면에서 ROLE을 부여할 사용자를 선택 후 목록 상단에 **\[ROLE 관리]** 버튼을 클릭합니다.\


    <figure><img src="../.gitbook/assets/image (521).png" alt=""><figcaption></figcaption></figure>
3.  부여할 ROLE을 선택합니다.

    * 시스템 관리자 : SDDC 플랫폼 시스템 접근 및 관리를 위한 ROLE입니다.
    * 관리자 : SDDC 플랫폼 관리 및 운영을 위한 ROLE입니다.
    * 사용자 :  SDDC 플랫폼 운영을 위한 ROLE입니다.\


    <div align="center">

    <figure><img src="../.gitbook/assets/image (523).png" alt=""><figcaption></figcaption></figure>

    </div>
4.  팝업 창 우측 하단의 **\[승인]** 버튼을 클릭합니다.\


    <div align="center">

    <figure><img src="../.gitbook/assets/image (524).png" alt=""><figcaption></figcaption></figure>

    </div>
5. 팝업 창이 닫히고, 승인된 사용자는 사용자 관리 화면에서 확인이 가능합니다.

## FAQ

> **Q. 시스템 관리자 ROLE 승인은 어떻게 등록하나요?**
>
> **A.** 시스템 관리자 ROLE의 경우, 시스템 관리자(sddc.ktcloud@kt.com)에게 요청하시기를 바랍니다.
