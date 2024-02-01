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

# NFV Subnet

***

## 개요

NFV Subnet 은 NFV Instance 를 생성시 VNF인터페이스에서 사용할 목적의 Subnet 입니다. 생성 시, NFV 인터페이스 유형이 지정되고 이에 따라 NFV Instance 내 용도가 구분됩니다.

### NFV 인터페이스 유형

<table><thead><tr><th>NFV Interface 유형 이름</th><th width="494">설명</th></tr></thead><tbody><tr><td>INT</td><td>서비스 네트워크 목적의 인터페이스 입니다.</td></tr><tr><td>EXT</td><td>서비스 네트워크 목적의 인터페이스 입니다.</td></tr><tr><td>HeartBeat</td><td>HeartBeat 목적의 인터페이스 입니다.</td></tr><tr><td>Mgmt</td><td>관리망 목적의 인터페이스 입니다.</td></tr></tbody></table>

## 사용 가이드

### NFV Subnet 목록 조회

전체 NFV Subnet 을 조회하는 기능입니다.

왼쪽 메뉴에서 'VNF 관리 > VNF > NFV Subnet' 을 클릭하여 NFV Subnet 목록을 조회합니다.\\

<figure><img src="../../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>

### NFV Subnet 생성

NFV Subnet 을 생성하는 기능입니다.

1. 왼쪽 메뉴에서 'VNF 관리 > VNF > NFV Subnet' 을 클릭하여 NFV Subnet 목록을 조회합니다.
2. NFV Subnet 목록 화면이 나타나면 상단 메뉴 중 생성 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (184).png" alt=""><figcaption></figcaption></figure>

3. NFV Subnet 생성 정보 입력합니다.
   * Subnet 이름: 생성할 NFV Subnet 의 이름입니다.
   * Tenant 이름 : NFV Subnet 이 생성될 Tenant 이름입니다.
   * VPC 이름 : NFV Subnet 이 생성될 VPC 이름입니다.
   * NFV 인터페이스 유형 : NFV 인터페이스 유형 정보로 이에 따라 NFV Instance 내 용도가 지정됩니다.
   * NFV Address Pool : NFV Subnet 의 Address 는 선택된 NFV Address Pool 내에서 자동으로 할당 됩니다.
   * NFV Farm 이름: NFV Subnet 생성 시 사용할 NFV Farm 정보입니다.
   * 설명: 생성할 NFV Subnet 에 대한 상세한 설명입니다.
4. 우측 하단 생성 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

5. NFV Subnet 목록에서 생성한 NFV Subnet 의 정상 상태를 확인합니다.

### NFV Subnet 수정

NFV Subnet 을 수정하는 기능입니다. 설명 정보만 수정 가능합니다.

1. 왼쪽 메뉴에서 'VNF 관리 > VNF > NFV Subnet' 을 클릭하여 NFV Subnet 목록을 조회합니다.
2. NFV Subnet 목록 화면이 나타나면 상단 메뉴 중 수정 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (185).png" alt=""><figcaption></figcaption></figure>

3. NFV Subnet 수정 정보를 입력합니다.
   * 설명: NFV Subnet 에 대한 상세한 설명입니다.
4. 우측 하단의 수정 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure>

5. NFV Subnet 목록에서 수정한 내용이 반영된 것을 확인합니다.

### NFV Subnet 삭제

NFV Subnet 을 삭제하는 기능입니다.

> **참고**
>
> * NFV Instance 에서 사용중인 경우 삭제할 수 없습니다.

1. 왼쪽 메뉴에서 'VNF 관리 > VNF > NFV Subnet' 을 클릭하여 NFV Subnet 목록을 조회합니다.
2. NFV Subnet 목록 화면이 나타나면 삭제할 NFV Subnet 을 선택한 후 상단 메뉴 중 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (186).png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (188).png" alt="" width="375"><figcaption></figcaption></figure>

4. 삭제 팝업 창이 닫히고, NFV Subnet 목록에서 "삭제중" 상태를 확인합니다.

## FAQ
