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

# Tenant 관리

***

## 개요

Tenant는 서비스 정책을 관리하는 최상위 그룹입니다.

* 사용자는 최대 1개의 Tenant를 생성 할 수 있으며, 공유를 받는데는 제약이 없습니다.
* Tenant 공유는 Tenant 권한 관리 메뉴에서 가능합니다.

### Tenant 유형

다음 3가지 유형의 Tenant가 존재합니다.

<table><thead><tr><th width="135.83595113438045">Tenant 유형</th><th width="359">설명</th><th>예시</th></tr></thead><tbody><tr><td>SYSTEM</td><td>시스템 관리자가 관리할 Tenant 유형입니다.</td><td>NFV, CISCO ACI 등 초기 환경 구축 시 사용하는 유형입니다.</td></tr><tr><td>ADMIN</td><td>관리자가 관리할 Tenant 유형입니다.</td><td>-</td></tr><tr><td>USER</td><td>사용자가 Tenant를 생성하면 부여되는 유형입니다.</td><td>-</td></tr></tbody></table>

### Tenant 자격

다음 2가지의 Tenant 자격이 존재합니다.

{% hint style="info" %}
**참고**

* 시스템 관리자와 관리자의 경우, Tenant 자격과 별도로 모든 유형에서 Tenant 권한 공유 기능이 가능합니다.&#x20;
* 사용자는 아래 자격에 따라 Tenant 권한 공유 기능이 제약됩니다.
{% endhint %}

<table><thead><tr><th width="118">자격 유형</th><th width="175.59259259259258">Tenant 권한 공유</th><th>설명</th></tr></thead><tbody><tr><td>소유자</td><td>가능</td><td>Tenant를 최초 생성한 사용자에게 부여되는 자격입니다.</td></tr><tr><td>구성원</td><td>불가</td><td>Tenant를 공유 받은 사용자에게 부여되는 자격입니다.</td></tr></tbody></table>

## 사용자 가이드

### Tenant 최초 생성

최초 로그인한 사용자가 플랫폼 초기 Tenant를 생성하는 기능입니다.

1. 사용자가 로그인 화면에서 로그인을 수행합니다.
2. Tenant 생성 팝업 창이 나타나면, Tenant 생성 정보를 입력합니다.
   * Tenant 이름 : Tenant 이름을 입력합니다.
   * 설명 : Tenant 설명을 입력합니다.
   * Default Network 설정
     * default VPC : Tenant 생성 시, default VPC 를 자동으로 생성합니다.
     * default Subnet : Tenant 생성 시, default VPC 하위에 default Subnet 를 자동으로 생성합니다.
3. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src=".gitbook/assets/스크린샷 2024-01-30 오후 3.34.01.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창이 닫히고 Tenant가 생성된 후 대시보드 화면으로 전환됩니다.

<figure><img src=".gitbook/assets/스크린샷 2024-02-01 오후 5.55.02.png" alt=""><figcaption></figcaption></figure>

### Tenant 목록 조회

메뉴에서 Tenant 옆의 더보기 아이콘을 클릭하여 나오는 Tenant 관리 메뉴를 클릭하여 Tenant 목록을 조회합니다.

<figure><img src=".gitbook/assets/스크린샷 2024-02-01 오후 5.55.34.png" alt=""><figcaption></figcaption></figure>

### Tenant 공유 권한 확인

소유 또는 공유된 Tenant 에 대한 모든 권한을 조회하는 기능입니다.

{% hint style="info" %}
**참고**

* 소유한 Tenant 는 모든 권한이 조회됩니다.
* 공유된 Tenant 에 대한 조회 권한은 기본적으로 부여 되며 권한 목록에서 노출되지 않습니다.
{% endhint %}

1. 메뉴에서 Tenant 옆의 더보기 아이콘을 클릭합니다.
2. Tenant 관리 메뉴를 클릭하여 Tenant 목록을 조회합니다.

<figure><img src=".gitbook/assets/스크린샷 2024-02-01 오후 5.55.48.png" alt=""><figcaption></figcaption></figure>

3. 화면에서 권한 조회할 Tenant를 선택 후 목록 상단에서 **\[공유 권한 확인]** 버튼을 클릭합니다.
4. 팝업 창에서 공유 받은 권한을 확인합니다.

<figure><img src=".gitbook/assets/스크린샷 2024-02-01 오후 5.55.55.png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. Tenant 생성이 불가능합니다.**
>
> **A.**  사용자 계정 당 최대 1개의 Tenant 생성이 가능합니다. 한 계정에서 여러 Tenant 접근하기 위해선 Tenant 권한을 공유해야합니다.
