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

# Subnet 관리

***

## 개요

Subnet 은 [VPC](../../network/vpc.md) 내 세분화된 네트워크 영역으로, VPC IP 주소 범위 내 세분화된 주소를 갖습니다.

SDDC 플랫폼 통해 생성된 모든 Subnet 를 조회, 수정, 삭제할 수 있고, USER, SYSTEM 유형의 Subnet를 생성할 수 있는 관리자 서비스입니다.

### Subnet 유형

<table><thead><tr><th width="174">유형</th><th>설명</th></tr></thead><tbody><tr><td>USER</td><td>일반 사용자 용 Subnet 유형.</td></tr><tr><td>SYSTEM</td><td>특수 목적 Subnet 유형.</td></tr><tr><td>NAS</td><td>NAS 서비스 용 Subnet 유형.</td></tr><tr><td>NFV</td><td>NFV 서비스 용 Subnet 유형.</td></tr></tbody></table>



## 사용 가이드

### Subnet 목록 조회

메뉴에서 시스템 관리 > 리소스 관리 > Subnet 관리 를 클릭하여 Subnet 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.39.42.png" alt=""><figcaption></figcaption></figure>

### Subnet 검색 조회

1. 시스템 관리 > 리소스 관리 > Subnet 관리 메뉴를 클릭합니다.
2. 검색 조건을 입력합니다. (각 조건은 And 로 적용됩니다.)
   * Subnet 유형 : Subnet 유형을 선택합니다.
   * Subnet 이름 : Subnet 이름을 입력합니다. 입력값을 포함한 경우 조회됩니다.
   * Subnet 주소 : IP 주소 범위를 입력합니다. 입력값을 포함한 경우 조회됩니다.
   * VPC 이름 : Subnet 이 생성된 VPC 이름을 입력합니다.  입력값을 포함한 경우 조회됩니다.
   * Tenant 이름 : Subnet 이 생성된 Tenant 이름을 입력합니다.  입력값을 포함한 경우 조회됩니다.
3. **\[돋보기]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.40.00.png" alt=""><figcaption></figcaption></figure>

2. 조건에 해당하는 Subnet 목록이 조회됩니다.

### Subnet 생성

메뉴에 선택된 Tenant 내 Subnet 을 생성하는 기능입니다.

{% hint style="info" %}
**참고**

* VLAN 번호는 Subnet 용 PathGroup 정보에 유효한 값만 가능합니다.
{% endhint %}

1. 시스템 관리 > 리소스 관리 > Subnet 관리 메뉴를 클릭합니다.
2. 목록 상단에서 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.40.18.png" alt=""><figcaption></figcaption></figure>

3. 생성 팝업 창에서 정보를 입력 및 선택합니다.
   * Subnet 유형 : Subnet 유형을 선택합니다.
   * Subnet 이름 : Subnet 이름을 입력합니다.
   * VPC : Subnet 이 생성될 VPC 를 선택합니다.
   * Subnet 주소 : Subnet 의 IP 주소 범위를 입력합니다.
   * VLAN 번호 : Subnet 에 할당할 VLAN 번호를 입력합니다.
   * 설명 : 설명을 입력합니다.
4. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.41.22.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 잠시 후 생성한 Subnet를 화면에서 확인 할 수 있습니다.

### Subnet 수정

1. 시스템 관리 > 리소스 관리 > Subnet 관리 메뉴를 클릭합니다.
2. 화면에서 수정할 Subnet 를 선택 후 목록 상단에서 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.40.40.png" alt=""><figcaption></figcaption></figure>

3. 수정 팝업 창에서 정보를 입력 및 선택합니다.
   * 설명 : 설명을 입력합니다.
4. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.41.31.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 잠시 후 수정한 Subnet를 화면에서 확인 할 수 있습니다.

### Subnet 삭제

1. 시스템 관리 > 리소스 관리 > Subnet 관리 메뉴를 클릭합니다.
2. 화면에서 삭제 할 Subnet 를 선택 후 목록 상단에서 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.40.54.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.41.42.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, 잠시 후 화면에서 확인 할 수 있습니다.

## FAQ

> **Q.**&#x20;
>
> A. &#x20;
