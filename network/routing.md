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

# Routing

***

## 개요

Routing 은 하나의 VPC 내 Subnet 간 통신을 위한 기능입니다.

[Subnet](subnet.md) 은 독립된 네트워크 공간으로 동일한 VPC 내 존재하더라도 기본적으로 서로 통신이 불가능하지만\
Routing Table 에 [Subnet](subnet.md) 을 등록하면 등록된 Subnet 간 통신이 가능하게 됩니다.

## 사용 가이드

### Routing 목록 조회

Tenant 내 Routing 을 조회하는 기능입니다.

메뉴에서 Network > Routing 을 클릭하여 Routing 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Routing 생성

하나의 VPC 내 Subnet 들을 연결하여 통신 관계를 생성하는 기능입니다.

1. 메뉴에서 Network > Routing 을 클릭하여 Routing 목록을 조회합니다.
2. 상단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. Routing 생성 정보를 입력합니다.
   * Routing 이름 : Routing 이름입니다.
   * 설명 : Routing 에 대한 상세한 설명입니다.
   * VPC : Routing이 생성되는 소속 VPC 입니다.
   * Subnet 목록 : Routing Table 에 등록할 Subnet 목록으로, 복수 개 선택이 가능합니다.
4. 팝업창 우측 하단 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (481).png" alt="" width="375"><figcaption></figcaption></figure>

5. Routing 목록에서 생성한 Routing 을 확인합니다.

### Routing 수정

Routing 정보를 수정하는 기능으로, Routing 설명을 수정할 수 있습니다.

1. 메뉴에서 Network > Routing 를 클릭하여 Routing 목록을 조회합니다.
2. 수정할 Routing 선택 후, 상단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. Routing 수정 정보를 입력합니다.
4. 팝업창 우측 하단 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (483).png" alt="" width="375"><figcaption></figcaption></figure>

5. Routing 목록에서 수정한 Routing의 수정 사항을 확인합니다.

### Routing Table 관리

Routing에 등록된 Routing Table 내의 Subnet 목록을 추가/삭제 할 수 있습니다.

1. 메뉴에서 Network > Routing 를 클릭하여 Routing 목록을 조회합니다.
2. Routing Table 을 관리할 Routing 선택 후, 상단의 **\[Routing Table 관리]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (5) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. Routing Table 내 Routing 대상 Subnet 목록을 수정합니다.
   * Subnet 추가 : Subnet을 선택 후, **\[추가]** 버튼을 클릭합니다.
   * Subnet 삭제 : 삭제할 Subnet 우측 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (6) (1) (1).png" alt="" width="453"><figcaption></figcaption></figure>

4. Routing Table 의 Routing 대상 Subnet 목록 수정 사항을 확인합니다.

### Routing 삭제

1. 메뉴에서 Network > Routing 를 클릭하여 Routing 목록을 조회합니다.
2. 삭제할 Routing를 선택한 다음, 상단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

3. 팝업창 우측 하단 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (8) (1).png" alt="" width="336"><figcaption></figcaption></figure>

4. Routing 목록에서 Routing 삭제 여부를 확인합니다.

## FAQ

> **Q. Routing 생성이 되지 않습니다.**
>
> **A.** [Routing 생성](routing.md#routing-1) 을 참고해주시기 바랍니다.  Routing 생성 절차대로 진행했음에도 생성되지 않는다면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
