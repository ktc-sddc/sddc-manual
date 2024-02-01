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

# Device

***

## 개요

Device 는 SDDC Platform 내에서 [NFV Instance](nfv-instance.md) 를 사용하기 위해 캡슐화한 리소스입니다. Device 는 [Service Graph](service-graph.md) 에 등록되어 사용됩니다.

## 사용 가이드

### Device 목록 조회

전체 Device 목록을 조회하는 기능입니다.

왼쪽 메뉴에서 VNF관리 > VNF > Device 를 클릭하여 현재 배포된 Device 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

### Device 상세 조회

Device 목록 화면에서 특정 Device를 선택하면 상세 정보를 확인할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (172).png" alt=""><figcaption></figcaption></figure>

### Device 등록

Device 를 등록하는 기능입니다.

1. 왼쪽 메뉴에서 VNF관리 > VNF > Device 를 클릭하여 현재 배포된 Device 목록을 조회합니다.
2. 좌측 상단의 등록 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (169).png" alt=""><figcaption></figcaption></figure>

3. Device 등록 정보를 입력합니다.
   * Device 이름: 생성할 Device 이름입니다.
   * NFV Instance 이름: 캡슐화할 NFV Instance 이름입니다.
4. 팝업창 우측 하단의 등록 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (164).png" alt=""><figcaption></figcaption></figure>

5. Device 목록에서 생성한 Device 를 확인합니다.

### Device 삭제

Device 를 삭제하는 기능입니다.

> **참고.**
>
> * Device 가 Service Graph 에 등록돼있는 경우 삭제가 불가능합니다.

1. 왼쪽 메뉴에서 VNF관리 > VNF > Device 를 클릭하여 현재 배포된 Device 목록을 조회합니다.
2. 삭제 하려는 Device 를 선택한 후, 좌측 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (168).png" alt=""><figcaption></figcaption></figure>

3. 팝업창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (173).png" alt="" width="375"><figcaption></figcaption></figure>

4. Device 목록에서 삭제한 Device 를 확인합니다.

### 정책 추가

> **참고**
>
> * 정책에 설정하지 않은 접근은 기본적으로 모두 거부(차단)됩니다.
> * 정책은 생성한 순서대로 정렬됩니다(가장 마지막에 생성한 정책이 가장 아래에 위치합니다).

> **주의**
>
> * 동일한 이름의 정책은 생성이 불가합니다.

1. 왼쪽 메뉴에서 VNF 관리 > VNF > Device 를 클릭합니다.
2. Device 목록에서 정책 생성을 진행할 Device 를 선택 후, 상단의 정책 관리 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure>

3. 정책 관리를 위한 팝업 창이 나타나면, 우측 상단의 추가 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure>

4. vFW 정책 추가를 위한 팝업 창이 나타나면, 정책 추가 내용을 입력합니다.
   * 정책 이름 : vFW 정책 이름을 입력합니다.
   * Source IP : Interface 유형(INT, EXT)과 입력 유형(Subnt, IP 범위)를 선택한 다음, Source IP Address를 입력합니다.
   * Destination IP : Interface 유형(INT, EXT)과 입력 유형(Subnt, IP 범위)를 선택한 다음, Destination IP Address를 입력합니다.
   * Protocol 정보 : Protocol를 선택한 다음, 각 Protocol에 맞는 하위 정보를 입력합니다.
     * TCP, UDP : Port 정보를 입력합니다.
     * ICMP : ICMP Type과 ICMP Code를 입력합니다.
     * IP : IP Protocol Number를 입력합니다.
   * 트래픽 허용 여부 : 생성할 vFW 정책의 트래픽 허용 여부를 선택합니다.
5. 입력이 완료되면, 추가 버튼을 클릭하여 정책 추가를 완료합니다.

<figure><img src="../../.gitbook/assets/image (176).png" alt=""><figcaption></figcaption></figure>

6. vFW 정책 추가 팝업 창이 닫히고, 정책관리 팝업 창에서 생성한 vFW 정책 상태를 확인합니다. 정상적으로 생성되면 "생성중"에서 "정상"으로 상태값이 전환됩니다.

<figure><img src="../../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure>

### 정책 삭제

1. 왼쪽 메뉴에서 VNF 관리 > VNF > Device 를 클릭합니다.
2. Device 목록에서 정책 삭제를 진행할 Device 를 선택 후, 상단의 정책 관리 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (178).png" alt=""><figcaption></figcaption></figure>

3. 정책 관리 팝업 창이 나타나면, 삭제할 정책을 선택한 다음 우측 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (175).png" alt=""><figcaption></figcaption></figure>

4. vFW 정책 삭제 팝업 창이 나타나면, 삭제할 정책의 이름을 확인한 다음 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (177).png" alt="" width="375"><figcaption></figcaption></figure>

5. vFW정책 삭제 팝업 창이 닫히고, 정책 관리 팝업 창에서 vFW 정책이 삭제되었는지 확인합니다. "삭제중" 상태에서 테이블 행이 완전히 삭제됩니다.

<figure><img src="../../.gitbook/assets/image (213).png" alt=""><figcaption></figcaption></figure>
