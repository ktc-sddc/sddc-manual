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

# 공통코드 관리

***

## 개요

플랫폼 내부 시스템에서 사용하는 코드그룹과 코드를 시스템 관리자가 관리합니다.

#### 코드 그룹과 코드

<table><thead><tr><th width="201.09580838323353">구분</th><th>설명</th></tr></thead><tbody><tr><td>코드 그룹</td><td>연관성이 있는 여러 개의 코드를 하나로 관리하기 위한 그룹을 의미합니다.</td></tr><tr><td>코드</td><td>시스템에서 사용하는 하나의 단위를 의미합니다.</td></tr></tbody></table>

## 사용자 가이드

### 코드 목록 조회

1. 시스템 관리 > 운영 정책 관리 > 공통코드 관리를 클릭합니다.
2. 코드 그룹을 조회합니다. 코드는 코드 그룹 선택 후 조회합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 5.56.52.png" alt=""><figcaption></figcaption></figure>

### 코드 그룹 생성

연관성이 있는 여러 개의 코드를 하나로 관리하기 위한 코드 그룹을 생성합니다.

1. 시스템 관리 > 운영 정책 관리 > 공통코드 관리 메뉴를 클릭합니다.
2. 코드 그룹 영역의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-01 오후 6.22.13.png" alt=""><figcaption></figcaption></figure>

3. 생성 팝업 창에서 정보를 입력 및 선택합니다.
   * 코드 그룹 ID : 규칙에 맞게 코드 그룹을 입력합니다.
   * 코드 그룹 이름 : 코드 그룹 이름을 입력합니다.
   * 사용 여부 : 사용 또는 미사용 선택이 가능합니다.
   * 설명 : 해당 코드 그룹의 설명을 작성합니다.
4. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (281).png" alt="" width="375"><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 생성한 코드 그룹을 코드 그룹 영역에서 확인 할 수 있습니다.

### 코드 그룹 수정

코드 그룹의 이름, 사용 여부, 설명을 수정합니다.

1. 시스템 관리 > 운영 정책 관리 > 공통코드 관리 메뉴를 클릭합니다.
2. 코드 그룹 영역의 수정할 코드 그룹을 선택 후 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-01 오후 6.23.12.png" alt=""><figcaption></figcaption></figure>

3. 수정 팝업 창에서 정보를 입력 및 선택합니다.
   * 코드 그룹 이름 : 코드 그룹 이름을 입력합니다.
   * 사용 여부 : 사용 또는 미사용 선택이 가능합니다.
   * 설명 : 해당 코드 그룹의 설명을 작성합니다.
4. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-01 오후 6.30.02.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 수정한 코드 그룹을 코드 그룹 영역에서 확인 할 수 있습니다.

### 코드 그룹 삭제

코드 그룹을 삭제합니다.

{% hint style="danger" %}
**주의**

코드 그룹 삭제 시, 시스템에 영향을 줄 수 있으므로 이슈 분석 후 신중히 삭제하시기 바랍니다.
{% endhint %}

1. 시스템 관리 > 운영 정책 관리 > 공통코드 관리 메뉴를 클릭합니다.
2. 코드 그룹 영역의 삭제할 코드 그룹을 선택 후 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-01 오후 6.23.37.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-01 오후 6.30.12.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, 삭제한 코드 그룹을 코드 그룹 영역에서 확인 할 수 있습니다.

### 코드 생성

코드 그룹 내 코드를 생성합니다.

1. 시스템 관리 > 운영 정책 관리 > 공통코드 관리 메뉴를 클릭합니다.
2. 코드 그룹 영역에서 코드 그룹을 선택하면 코드 영역에 해당 코드그룹에 속한 코드가 조회됩니다.
3. 이후 코드 영역의 생성 버튼이 활성화 됩니다. **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-01 오후 6.22.48.png" alt=""><figcaption></figcaption></figure>



4. 생성 팝업 창에서 정보를 입력 및 선택합니다.
   * 코드 : 코드를 입력합니다.
   * 코드 이름 : 코드 이름을 입력합니다.
   * 사용 여부 : 사용 또는 미사용 선택이 가능합니다.
   * 정렬 : 0\~9까지 숫자 선택이 가능합니다. 조회 정렬을 의미하며 오름차순 정렬됩니다. 숫자가 같다면 최근 수정된 코드가 우선됩니다.
   * 설명 : 해당 코드 그룹의 설명을 작성합니다.
5. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (287).png" alt="" width="375"><figcaption></figcaption></figure>

6. 팝업 창이 닫히고, 생성한 코드를 코드 영역에서 확인 할 수 있습니다.

### 코드 수정

코드 그룹 내 코드 정보를 수정합니다.

1. 시스템 관리 > 운영 정책 관리 > 공통코드 관리 메뉴를 클릭합니다.
2. 코드 그룹 영역에서 코드 그룹을 선택하면 코드 영역에 해당 코드그룹에 속한 코드가 조회됩니다.
3. 수정할 코드를 선택 후 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-01 오후 6.24.12.png" alt=""><figcaption></figcaption></figure>

4. 수정 팝업 창에서 정보를 입력 및 선택합니다.
   * 코드 : 코드를 입력합니다.
   * 코드 이름 : 코드 이름을 입력합니다.
   * 사용 여부 : 사용 또는 미사용 선택이 가능합니다.
   * 정렬 : 0\~9까지 숫자 선택이 가능합니다. 조회 정렬을 의미하며 오름차순 정렬됩니다. 숫자가 같다면 최근 수정된 코드가 우선됩니다.
   * 설명 : 해당 코드 그룹의 설명을 작성합니다.
5. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-01 오후 6.30.28.png" alt=""><figcaption></figcaption></figure>

6. 팝업 창이 닫히고, 수정한 코드는 코드 영역에서 확인 할 수 있습니다.

### 코드 삭제

시스템 내부적으로 사용하고 있는 코드를 삭제합니다.

{% hint style="danger" %}
**주의**

코드 삭제 시, 시스템에 영향을 줄 수 있으므로 이슈 분석 후 신중히 삭제하시기 바랍니다.
{% endhint %}

1. 시스템 관리 > 운영 정책 관리 > 공통코드 관리 메뉴를 클릭합니다.
2. 화면에서 코드 영역의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-01 오후 6.24.27.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-01 오후 6.30.38.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, 삭제한 코드를 코드 영역에서 확인 할 수 있습니다.

## FAQ

> **Q. 시스템 관리자 ROLE 승인은 어떻게 등록하나요?**
>
> **A.** 시스템 관리자 ROLE의 경우, 시스템 관리자(sddc.ktcloud@kt.com)에게 요청하시기를 바랍니다.
