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

SDDC 플랫폼 통해 생성된 모든 Tenant 를 조회, 수정, 삭제할 수 있고, 모든 유형의 Tenant를 생성할 수 있는 관리자 서비스입니다.

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

### Tenant 목록 조회

시스템 관리 > 리소스 관리 > Tenant 관리 메뉴를 클릭하여 Tenant 목록을 조회합니다.\
(왼쪽 상단의 Tenant 옆의 더보기 아이콘을 클릭하여 나오는 Tenant 관리 메뉴로도 가능합니다.)

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 5.57.44.png" alt=""><figcaption></figcaption></figure>

### Tenant 생성

시스템 관리자와 관리자인 경우에만 사용 가능한 기능으로, 새로운 Tenant를 생성합니다.

현재 접속한 사용자의 ROLE에 따라 생성 가능한 Tenant 유형은 다음과 같습니다.

<table><thead><tr><th width="292.12060301507535">ROLE</th><th>생성 가능한 Tenant 유형</th></tr></thead><tbody><tr><td>시스템 관리자</td><td>SYSTEM, ADMIN, USER</td></tr><tr><td>관리자</td><td>ADMIN, USER</td></tr></tbody></table>

1. 시스템 관리 > 리소스 관리 > Tenant 관리 메뉴를 클릭합니다.
2. 목록 상단에서 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 3.03.26.png" alt=""><figcaption></figcaption></figure>

3. 생성 팝업 창에서 정보를 입력 및 선택합니다.
   * Tenant 유형 : SYSTEM, ADMIN, USER 중에 선택합니다.
     * SYSTEM을 선택하면 'ACI Tenant 이름' 입력창이 새로 추가됩니다. CISCO ACI 이름을 확인 후 정확하게 입력합니다.
   * 이름 : Tenant 이름을 입력합니다.
   * 설명 : Tenant 설명을 입력합니다.
4. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (294).png" alt="" width="375"><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 잠시 후 생성한 Tenant를 화면에서 확인 할 수 있습니다.

### Tenant 수정

Tenant 설명 정보를 수정합니다.

1. 시스템 관리 > 리소스 관리 > Tenant 관리 메뉴를 클릭합니다.
2. 화면에서 삭제 할 Tenant를 선택 후 목록 상단에서 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 3.04.35.png" alt=""><figcaption></figcaption></figure>

3. 수정 팝업 창에서 정보를 입력합니다.
   * 설명 : 설명을 입력합니다.
4. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-30 오후 1.41.43.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창이 닫히고, 잠시 후 수정한 Tenant 정보를 화면에서 확인 할 수 있습니다.

### Tenant 삭제

Tenant를 삭제합니다. 삭제된 Tenant는 복구가 불가능 하며 신중히 삭제해주시기를 바랍니다.

{% hint style="info" %}
**참고**

* 삭제된 Tenant는 복구가 불가능 하며 신중히 삭제해주시기를 바랍니다.
* Tenant 내부에 Server, Volume, VPC, OSP Network 등을 사용하고 있는 오브젝트가 존재 할 경우 삭제가 불가합니다. 해당 오브젝트를 삭제 후 Tenant를 삭제해주시기를 바랍니다.
{% endhint %}

1. 시스템 관리 > 리소스 관리 > Tenant 관리 메뉴를 클릭합니다.
2. 화면에서 삭제 할 Tenant를 선택 후 목록 상단에서 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 3.04.10 (1).png" alt=""><figcaption></figcaption></figure>

3. 삭제 팝업 창에서 정보를 입력합니다.
4. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 3.04.46.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 잠시 후 화면에서 확인 할 수 있습니다.

### Tenant 생성 (IPC 연동)

IPC 포털 내 Openstack Project 를 SDDC Platform 과 연동하여 Tenant 를 생성합니다.

{% hint style="info" %}
**참고**

* Tenant 이름은 선택한 Openstack Project 이름으로 자동 등록됩니다.
* 이미 연동된 Openstack Project는 목록에서 조회되지 않습니다.
* 생성된 Tenant 유형은 USER 입니다.
{% endhint %}

1. 시스템 관리 > 리소스 관리 > Tenant 관리 메뉴를 클릭합니다.
2. 목록 상단에서 **\[생성 (IPC 연동)]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 3.01.37.png" alt=""><figcaption></figcaption></figure>

3. 생성 팝업 창에서 정보를 입력 및 선택합니다.
   * OSP Project 이름 : 연동할 Openstack Project 를 선택합니다.
   * 설명 : Tenant 설명을 입력합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 3.00.26.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.
5. 팝업 창이 닫히고, 잠시 후 생성한 Tenant를 화면에서 확인 할 수 있습니다.

## FAQ

> **Q. SYSTEM 유형 Tenant가 삭제 되지 않습니다.**
>
> **A.** 사용자의 ROLE이 시스템 관리자인 경우에만 삭제가 가능합니다. 현재 접속한 계정의 ROLE을 다시 한번 확인해주시기 바랍니다. 시스템 관리자 계정인 경우에도 삭제가 불가능 할 시, 시스템 관리자(sddc.ktcloud@kt.com)에게 요청하시기를 바랍니다.
