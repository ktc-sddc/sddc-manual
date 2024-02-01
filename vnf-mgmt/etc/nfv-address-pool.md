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

# NFV Address Pool

***

## 개요

NFV Address Pool 은 NFV Subnet 에 할당할 Address 를 관리 및 제공하는 역할을 합니다. NFV 인터페이스 유형, Address Pool 그리고 Mask Bit 정보를 갖고 있습니다. 동일한 NFV 인터페이스 유형을 갖는 NFV Subnet에 Address 를 제공할 수 있으며, Address 는 Address Pool 범위 내에서 Mask Bit 크기에 맞춰 생성합니다.

## 사용 가이드

### NFV Address Pool 목록 조회

왼쪽 메뉴에서 'VNF 관리 > 기준 정보 > NFV Address Pool' 를 클릭하여 NFV Address Pool 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>

### NFV Address Pool 생성

1. 왼쪽 메뉴에서 'VNF 관리 > 기준 정보 > NFV Address Pool' 를 클릭하여 NFV Address Pool 목록을 조회합니다.
2. 좌측 상단의 생성 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

3. NFV Address Pool 생성 정보 입력합니다.
   * NFV 인터페이스 유형: NFV 인터페이스 유형 정보로 동일한 유형을 갖는 NFV Subnet 을 구분하는 정보가 됩니다.
   * NFV Address Pool 이름: 생성할 NFV Address Pool 의 이름입니다.
   * Address Pool: 생성할 NFV Address Pool 의 주소 범위가 되고, 해당 범위 내에서 Address 가 생성됩니다.
   * Mask Bit: 해당 Mask Bit 크기로 Address 가 생성됩니다.
4.  우측 하단의 생성 버튼을 클릭합니다.\\

    <figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>
5. NFV Address Pool 목록에서 생성 되었는지 확인합니다.

### NFV Address Pool 삭제

1. 왼쪽 메뉴에서 'VNF 관리 > 기준 정보 > NFV Address Pool' 를 클릭하여 NFV Address Pool 목록을 조회합니다.
2. NFV Address Pool 목록 화면이 나타나면 삭제할 NFV Address Pool 을 선택한 후 상단 메뉴 중 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (200).png" alt=""><figcaption></figcaption></figure>

3.  팝업 창 우측 하단의 삭제 버튼을 클릭합니다.\\

    <figure><img src="../../.gitbook/assets/image (69).png" alt="" width="375"><figcaption></figcaption></figure>
4. NFV Address Pool 목록에서 삭제 되었는지 확인합니다.

## FAQ

> **Q. NFV Address Pool 이 삭제되지 않습니다.**
>
> A. 사용 중인 Address 가 있는 경우 삭제할 수 없습니다.
