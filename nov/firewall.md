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

# 방화벽(이름 변경 -vFW)

***

## 개요

사용 가능한 vFW 목록을 관리하고, vFW 별 정책을 설정할 수 있는 기능을 제공합니다.

## 사용가이드

### vFW 조회

{% hint style="info" %}
**참고**

* vFW을 사용하려면 운영자에게 먼저 생성 요청을 해야 합니다.
* 생성을 원하시는 계정, Tenant, VPC를 sddc.ktcloud@kt.com 으로 생성 요청 메일을 보내주시면 됩니다.


{% endhint %}

사용가능한 vFW 목록을 조회합니다.

1. 왼쪽 메뉴에서 NFV > vFW 을 클릭합니다.
2. vFW 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

### vFW 상세 조회

1. 왼쪽 메뉴에서 NFV > vFW 을 클릭합니다.
2. vFW 목록에서 상세 조회할 vFW를 선택합니다.

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

### vFW 정책 추가

{% hint style="info" %}
**참고**

* 정책에 설정하지 않은 접근은 기본적으로 모두 거부(차단)됩니다.
* 정책은 생성한 순서대로 정렬됩니다. 가장 마지막에 생성한 정책이 가장 아래에 위치합니다.
* 동일한 이름의 정책은 생성이 불가합니다.
{% endhint %}

1. 왼쪽 메뉴에서 NFV > vFW 을 클릭합니다.
2. vFW 목록에서 정책 생성을 진행할 vFW 을 선택 후, 상단의 **\[정책 관리]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

3. 정책 관리를 위한 팝업 창이 나타나면, 팝업창 우측 상단의 **\[추가]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

4. vFW 정책 정보를 입력합니다.
   * 정책 이름을 입력합니다.
   * Source의 Interface: 해당 Source IP의 입력 유형과 IP를 입력합니다.
   * Destination의 Interface: 해당 Destination IP의 입력 유형과 IP를 입력합니다.
   * Protocol을 입력합니다.
   * 해당 정책의 트래픽 허용 여부를 입력합니다.
5. 입력이 완료되면, **\[추가]** 버튼을 클릭하여 정책 추가를 완료합니다.

<figure><img src="../.gitbook/assets/image (18).png" alt="" width="563"><figcaption></figcaption></figure>

6. vFW 정책 추가 팝업 창이 닫히고, 정책관리 팝업 창에서 생성한 vFW 정책 상태를 확인합니다. 정상적으로 생성되면 '생성중'에서 '정상'으로 상태값이 전환됩니다.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

### vFW 정책 삭제

1. 왼쪽 메뉴에서 NFV > vFW 을 클릭합니다.
2. vFW 목록에서 정책 삭제를 진행할 vFW 을 선택 후, 상단의 **\[정책 관리]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

3. 정책 관리를 위한 팝업 창이 나타나면, 삭제할 정책을 선택한 다음 우측 상단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

4. 삭제 확인 팝업 창에서 삭제할 정책의 이름을 확인하고, **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (15).png" alt="" width="375"><figcaption></figcaption></figure>

5. vFW정책 삭제 팝업 창이 닫히고, 정책 관리 팝업 창에서 vFW 정책이 삭제되었는지 확인합니다. '삭제중' 상태에서 테이블 행이 완전히 삭제됩니다.

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. 정책의 순서를 변경하고 싶습니다.**
>
> A. 현재는 정책의 순서 변경 기능을 지원하지 않고 있습니다. 정책을 삭제하고, 생성하여 주시기 바랍니다.

> **Q. 정책이 생성/삭제가 되지 않습니다.**
>
> A. 시스템 관리자(sddc.ktcloud@kt.com)에게 문의하시기 바랍니다.
