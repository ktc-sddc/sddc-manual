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

# Tenant 권한 관리

***

## 개요

Tenant는 서비스 정책을 관리하는 최상위 그룹입니다. 이러한 Tenant를 다른 사용자에게 메뉴/기능별로 권한을 공유할 수 있으며, 권한을 공유 받은 사용자는 Tenant 내 메뉴 접근이 가능해집니다.

**ROLE에 따른 Tenant 권한 관리 범위**

사용자 ROLE에는 3가지 유형이 존재하며, ROLE에 따라 Tenant 권한 공유 기능이 제약됩니다.

<table><thead><tr><th width="146">ROLE 유형</th><th>Tenant 권한 관리 범위</th></tr></thead><tbody><tr><td>시스템 관리자</td><td>모든 Tenant에 접근 가능하며, 관리자와 사용자에게 Tenant 권한을 부여할 수 있습니다.</td></tr><tr><td>관리자</td><td>모든 Tenant에 접근 가능하며, 사용자에 Tenant 권한을 부여할 수 있습니다.</td></tr><tr><td>사용자</td><td>본인이 소유자인 Tenant에 대해서만 다른 사용자에게 Tenant 권한을 부여할 수 있습니다.<br>※ 공유받은 Tenant의 경우 해당 Tenant 권한 메뉴는 사라집니다.</td></tr></tbody></table>

## 사용 가이드

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

<figure><img src=".gitbook/assets/image (496).png" alt=""><figcaption></figcaption></figure>

### Tenant 권한 조회

Tenant 권한 관리 메뉴를 클릭하여 현재 선택된 Tenant 의 권한을 공유 받은 사용자 목록을 조회합니다.

<figure><img src=".gitbook/assets/image (498).png" alt=""><figcaption></figcaption></figure>

### Tenant 권한 공유

소유자가 아닌 다른 사용자에게 Tenant 메뉴/기능 권한을 부여합니다.

1. Tenant 권한 관리 메뉴를 클릭합니다.
2. 목록 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src=".gitbook/assets/image (499).png" alt=""><figcaption></figcaption></figure>

3. 생성 팝업 창에서 정보를 선택합니다.
   * 사용자 정보 : 현재 선택된 Tenant의 권한을 부여할 사용자를 검색하여 등록합니다.
   * Tenant 권한 : 권한 그룹, 권한 그룹의 유형에 따라 권한을 세부적으로 부여할 수 있습니다.
4. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src=".gitbook/assets/스크린샷 2024-01-30 오후 2.02.49.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 화면 목록에서 권한을 부여받은 사용자를 확인 할 수 있습니다.

### Tenant 권한 수정

기존에 부여된 Tenant 메뉴/기능 권한을 추가 혹은 삭제할 수 있니다.

1. Tenant 권한 관리 메뉴를 클릭합니다.
2. 화면에서 Tenant 권한을 공유받은 사용자를 선택 후 목록 상단에 **\[수정]** 버튼을 클릭합니다.

<figure><img src=".gitbook/assets/image (500).png" alt=""><figcaption></figcaption></figure>

3. 수정 팝업 창에서 Tenant 권한 선택 목록을 변경합니다.
   * Tenant 권한 : 기존에 공유받은 권한은 선택되어 있으며, 필요에 따라 추가/삭제할 권한을 선택합니다.
4. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src=".gitbook/assets/image (501).png" alt="" width="375"><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 화면에서 확인 할 수 있습니다.

### Tenant 권한 삭제

사용자에게 부여된 Tenant 메뉴/기능 권한을 삭제합니다.

1. Tenant 권한 관리 메뉴를 클릭합니다.
2. 화면에서 Tenant 권한을 공유받은 사용자를 선택 후 목록 상단에 **\[삭제]** 버튼을 클릭합니다.

<figure><img src=".gitbook/assets/image (502).png" alt=""><figcaption></figcaption></figure>

3. 삭제 팝업 창에서 정보를 입력합니다.
   * Tenant 권한을 삭제할 사용자 ID를 입력합니다.
4. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src=".gitbook/assets/image (503).png" alt="" width="375"><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 화면에서 확인 할 수 있습니다.

## FAQ

> **Q. 선택된 Tenant에 내 권한은 보이지 않나요?**
>
> A. 다른 사용자에게 공유한 권한에 한해 목록이 보여지며, 내 권한은 기본으로 적용된 상태라 보이지 않습니다.
