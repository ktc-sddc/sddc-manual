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

# VPC 관리

***

## 개요

VPC(Virtual Private Cloud)는 논리적으로 격리된 가상의 네트워크에서 SDDC 플랫폼 리소스를 운영할 수 있는 기능을 제공합니다.

SDDC 플랫폼 통해 생성된 모든 VPC 를 조회, 수정, 삭제할 수 있고, Tenant 에 모든 유형의 VPC를 생성할 수 있는 관리자 서비스입니다.

### VPC 유형

<table><thead><tr><th width="204">유형</th><th>설명</th></tr></thead><tbody><tr><td>USER</td><td>일반 사용자 용 VPC 유형.</td></tr><tr><td>SYSTEM</td><td>특수 목적 VPC 유형.</td></tr></tbody></table>



## 사용 가이드

### VPC 목록 조회

메뉴에서 시스템 관리 > 리소스 관리 > VPC 관리 를 클릭하여 VPC 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.31.57.png" alt=""><figcaption></figcaption></figure>

### VPC 검색 조회

1. 시스템 관리 > 리소스 관리 > VPC 관리 메뉴를 클릭합니다.
2. 검색 조건을 입력합니다. (각 조건은 And 로 적용됩니다.)
   * VPC 유형 : VPC 유형을 선택합니다.
   * VPC 이름 : VPC 이름을 입력합니다. 입력값을 포함한 경우 조회됩니다.
   * IP 주소 범위 (CIDR) : IP 주소 범위를 입력합니다. 입력값을 포함한 경우 조회됩니다.
   * Tenant 이름 : VPC 가 생성된 Tenant 이름을 입력합니다.  입력값을 포함한 경우 조회됩니다.
3. **\[돋보기]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.32.13.png" alt=""><figcaption></figcaption></figure>

4. 조건에 해당하는 VPC 목록이 조회됩니다.

### VPC 생성

메뉴에 선택된 Tenant 내 VPC 를 생성하는 기능입니다.

1. 시스템 관리 > 리소스 관리 > VPC 관리 메뉴를 클릭합니다.
2. 목록 상단에서 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.32.26 (1).png" alt=""><figcaption></figcaption></figure>

3. 생성 팝업 창에서 정보를 입력 및 선택합니다.
   * VPC 유형 : VPC 유형을 선택합니다.
   * VPC 이름 : VPC 이름을 입력합니다.
   * IP 주소 범위(CIDR) : VPC 의 IP 주소 범위를 입력합니다.
   * 설명 : 설명을 입력합니다.
4. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.20.17.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 잠시 후 생성한 VPC를 화면에서 확인 할 수 있습니다.

### VPC 수정

1. 시스템 관리 > 리소스 관리 > VPC 관리 메뉴를 클릭합니다.
2. 화면에서 수정할 VPC 를 선택 후 목록 상단에서 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.32.58.png" alt=""><figcaption></figcaption></figure>

3. 수정 팝업 창에서 정보를 입력 및 선택합니다.
   * 설명 : 설명을 입력합니다.
4. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.20.57.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 잠시 후 수정한 VPC를 화면에서 확인 할 수 있습니다.

### VPC 삭제

1. 시스템 관리 > 리소스 관리 > VPC 관리 메뉴를 클릭합니다.
2. 화면에서 삭제 할 VPC를 선택 후 목록 상단에서 **\[삭제]** 버튼을 클릭합니다.
3. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.33.18.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, 잠시 후 화면에서 확인 할 수 있습니다.

## FAQ

> **Q. VPC 가 삭제가 안됩니다.**
>
> A. VPC 하위에 자원이 존재하는 경우 삭제가 불가능합니다. 해당 경우가 아니라면 시스템 관리자(sddc.kcloud@kt.com) 에게 문의바랍니다.
