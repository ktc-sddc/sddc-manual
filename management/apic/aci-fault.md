# ACI Fault

## 개요

ACI Fault 는 SDDC 플랫폼과 연동된 ACI 에서 발생중인 Fault 정보를 의미합니다. 플랫폼을 통해 생성된 Tenant 의 Fault 정보를 확인하여 네트워크 이상 유무를 확인할 수 있으며, Fault 와 연관된 SDDC 리소스 정보를 확인할 수 있습니다.



## 사용 가이드

### Fault 목록 조회

시스템 관리 > APIC 관리 > ACI Fault 메뉴를 클릭하여 ACI Fault 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.48.22.png" alt=""><figcaption></figcaption></figure>

### Fault 검색 조회

SDDC 플랫폼과 연관된 ACI Fault 정보를 검색 조회하는 기능입니다.

1. 시스템 관리 > APIC 관리 > ACI Fault 메뉴를 클릭합니다.
2. 검색 조건을 입력합니다. (각 조건은 And 로 적용됩니다.)
   * Tenant 이름 : 검색을 원하는 Tenant 이름을 입력합니다. 입력된 값이 포함된 Tenant를 조회합니다.
   * 리소스 유형 : 검색을 원하는 리소스 유형을 선택합니다. 리소스 유형이 일치하는 경우만 조회합니다.
3. **\[돋보기]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.48.40.png" alt=""><figcaption></figcaption></figure>

4. 조건에 해당하는 ACI Fault 목록이 조회합니다.

### Fault 상세 조회

ACI Fault 정보를 상세 조회하는 기능입니다.

1. 시스템 관리 > APIC 관리 > ACI Fault 메뉴를 클릭합니다.
2. 상세 조회를 원하는 Fault 를 선택 후 **\[상세]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.53.56 1.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창을 통해 상세 정보를 조회합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.49.56.png" alt=""><figcaption></figcaption></figure>

### 동기화

ACI Fault 정보를 실시간 동기화하는 기능입니다.\
(SDDC 플랫폼과 ACI 는 일정 주기를 가지고 동기화를 진행하고 있습니다.)

1. 시스템 관리 > APIC 관리 > ACI Fault 메뉴를 클릭합니다.
2. 목록 상단에서 **\[동기화]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 2.49.07.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[동기화]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-30 오후 4.42.11.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, 실시간 동기화 된 ACI Fault 전체 목록이 조회됩니다.
