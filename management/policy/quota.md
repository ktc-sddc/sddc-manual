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

# Quota 관리

***

## 개요

Quota 는 리소스 생성 한도를 의미하며, 이를 초과하여 리소스를 생성할 수 없습니다. 기본 Quota 는 플랫폼에 속한 Tenant 에 공통적으로 적용되는 Quota 입니다. Tenant Quota 는 Tenant 개별로 적용되는 Quota 를 의미하며 Tenant Quota 가 기본 Quota 보다 우선됩니다.

관리자는 기본 Quota를 통해 플랫폼 공통으로 적용되는 Quota 설정을 제어할 수 있고, Tenant 별 Quota 변경 요청을 관리할 수 있습니다.

#### 용어 설명

<table><thead><tr><th width="196.78411910669973">용어</th><th>설명</th></tr></thead><tbody><tr><td>Resource</td><td>Quota 제한 리소스를 의미.</td></tr><tr><td>Resource Scope</td><td>Quota 제한 범위를 의미.</td></tr><tr><td>Quota</td><td> Resource Scope 내 생성 가능한 리소스의 개수를 의미.</td></tr></tbody></table>



## 사용 가이드

### 기본 Quota 현황 조회

메뉴에서 시스템 관리 > 운영 정책 관리 > Quota 관리 를 클릭하여 기본 Quota 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 5.55.53.png" alt=""><figcaption></figcaption></figure>

### 기본 Quota 생성

기본 Quota 를 생성합니다.

{% hint style="info" %}
**참고**

* Resouce 별 최대 1개의 기본 Quota를 생성할 수 있습니다.
{% endhint %}

1. 메뉴에서 시스템 관리 > 운영 정책 관리 > Quota 관리 를 클릭하여 기본 Quota 목록을 조회합니다.
2. 목록 상단에서 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.54.02.png" alt=""><figcaption></figcaption></figure>

3. 생성 팝업 창에서 정보를 입력합니다.
   * Resource : 생성을 원하는 기본 Quota 대상 Resource 를 선택합니다.
   * Resource Scope : Resource 선택 시 자동으로 입력됩니다.
   * 기본 Quota : 원하는 Quota 값을 입력합니다.
4. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-30 오후 5.47.24.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 생성된 기본 Quota 가 목록에서 조회됩니다.

### 기본 Quota 수정

기본 Quota 의 Quota 값을 수정하는 기능입니다.

1. 메뉴에서 시스템 관리 > 운영 정책 관리 > Quota 관리 를 클릭하여 기본 Quota 목록을 조회합니다.
2. 수정을 원하는 기본 Quota 를 선택한 후 목록 상단에서 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.54.23.png" alt=""><figcaption></figcaption></figure>

3. 수정 팝업 창에서 정보를 입력합니다.
   * 기본 Quota : 원하는 Quota 값을 입력합니다.
4. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-30 오후 5.53.19.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 목록에서 수정한 정보를 확인할 수 있습니다.

### 기본 Quota 삭제

1. 메뉴에서 시스템 관리 > 운영 정책 관리 > Quota 관리 를 클릭하여 기본 Quota 목록을 조회합니다.
2. 삭제를 원하는 기본 Quota 를 선택한 후 목록 상단에서 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.54.40.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-30 오후 5.57.49.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 기본 Quota 목록에서 삭제된 것을 확인할 수 있습니다.

### Tenant Quota 현황 조회

메뉴에서 시스템 관리 > 운영 정책 관리 > Quota 관리 를 클릭 후 Tenant Quota 현황 탭을 선택하여 Tenant Quota 현황을 조회합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 5.56.07.png" alt=""><figcaption></figcaption></figure>

### Tenant Quota 생성

1. 메뉴에서 시스템 관리 > 운영 정책 관리 > Quota 관리 를 클릭합니다.
2. Tenant Quota 현황 탭을 클릭합니다.
3. 목록 상단에서 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.55.52.png" alt=""><figcaption></figcaption></figure>

4. 생성 팝업 창 내 정보를 입력합니다.
   * Tenant : Tenant Quota 가 적용될 Tenant 를 선택합니다.
   * Resource : 생성을 원하는 Tenant Quota 대상 Resource 를 선택합니다.
   * Resource Scope : Resource 선택 시 자동으로 입력됩니다.
   * Tenant Quota : 원하는 Quota 값을 입력합니다.
5. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.56.17.png" alt=""><figcaption></figcaption></figure>

6. 팝업 창이 닫히고, 목록에서 생성된 정보가 조회됩니다.

### Tenant Quota 수정

1. 메뉴에서 시스템 관리 > 운영 정책 관리 > Quota 관리 를 클릭합니다.
2. Tenant Quota 현황 탭을 클릭합니다.
3. 수정을 원하는 Tenant Quota 를 선택한 후 목록 상단 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.56.30.png" alt=""><figcaption></figcaption></figure>

4. 수정 팝업 창 내 정보를 입력합니다.
   * Tenant Quota : 원하는 Quota 값을 입력합니다.
5. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.56.42.png" alt=""><figcaption></figcaption></figure>

6. 팝업 창이 닫히고, 목록에서 수정된 정보가 조회됩니다.

### Tenant Quota 삭제

1. 메뉴에서 시스템 관리 > 운영 정책 관리 > Quota 관리 를 클릭합니다.
2. Tenant Quota 현황 탭을 클릭합니다.
3. 삭제를 원하는 Tenant Quota 를 선택한 후 목록 상단 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.56.56.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-06 오전 11.15.28.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 목록에서 정보가 삭제됩니다.

### 변경 요청 내역 조회

메뉴에서 시스템 관리 > 운영 정책 관리 > Quota 관리 를 클릭 후, 변경 요청 내역 탭을 선택하여 변경 요청 내역을 조회합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 5.56.17.png" alt=""><figcaption></figcaption></figure>

### 변경 요청 승인

1. 메뉴에서 시스템 관리 > 운영 정책 관리 > Quota 관리 를 클릭합니다.
2. 변경 요청 내역 탭을 클릭합니다.
3. 승인을 원하는 요청을 선택 후 목록 상단 **\[승인]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.59.46.png" alt=""><figcaption></figcaption></figure>

4. 승인 팝업 창 내 정보를 입력합니다.
   * 승인 메시지 : 요청자에게 전달할 메시지를 입력합니다.
5. 팝업 창 우측 하단의 **\[승인]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.59.59.png" alt=""><figcaption></figcaption></figure>

6. 팝업 창이 닫히고, 목록에서 정보가 변경됩니다.

### 변경 요청 반려

1. 메뉴에서 시스템 관리 > 운영 정책 관리 > Quota 관리 를 클릭합니다.
2. 변경 요청 내역 탭을 클릭합니다.
3. 반려를 원하는 요청을 선택 후 목록 상단 **\[반려]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.00.16.png" alt=""><figcaption></figcaption></figure>

4. 반려 팝업 창 내 정보를 입력합니다.
   * 반려 메시지 : 요청자에게 전달할 메시지를 입력합니다.
5. 팝업 창 우측 하단의 **\[반려]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.00.29.png" alt=""><figcaption></figcaption></figure>

6. 팝업 창이 닫히고, 목록에서 정보가 변경됩니다.
