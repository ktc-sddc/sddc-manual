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

# NFV Farm

***

## 개요

NFV Farm 은 VNF(인스턴스)가 배포될 오픈스택의 NFV전용 compute node의 정보를 관리합니다. 생성 위치(Farm) 따른 [VIM](vim.md) 정보와 네트워크 구성에 필요한 정보를 그룹화하여 관리합니다.

## 사용 가이드

### NFV Farm 목록 조회

전체 NFV Farm 목록을 조회하는 기능입니다.

왼쪽 메뉴에서 'VNF 관리 > 기준정보 > NFV Farm' 를 클릭하여 NFV Farm 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (201).png" alt=""><figcaption></figcaption></figure>

### NFV Farm 생성

NFV Farm 을 생성하는 기능입니다. NFV Farm을 생성하기 위해서는, [VIM](vim.md) 정보와 NFV 유형의 [PathGroup](../sdn/pathgroup.md) 이 사전에 등록되어 있어야 합니다.

1. 왼쪽 메뉴에서 'VNF 관리 > 기준정보 > NFV Farm' 를 클릭하여 NFV Farm 목록을 조회합니다.
2. 좌측 상단의 생성 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (202).png" alt=""><figcaption></figcaption></figure>

3. NFV Farm 생성 정보를 입력합니다.
   * NFV Farm 이름 : 생성될 NFV Farm의 이름입니다.
   * OSM VIM 이름 : OSM에 등록된 VIM 중에 사용할 VIM을 선택합니다.
   * NFV Farm Interface 구성 : VNF 생성에 필요한 Interface 정보를 설정합니다.
     * Network 유형 : SR-IOV, OVN 등의 네트워크 유형 선택합니다.
     * Physical Network 이름 : OpenStack에서 사용할 Physical Network 이름을 입력합니다.
     * PathGroup : Interface에 연관된 PathGroup을 선택합니다.
   * 설명 : NFV Farm 에 대한 상세한 설명입니다.
4.  팝업창 우측 하단 생성 버튼을 클릭합니다.\\

    <figure><img src="../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>
5. NFV Farm 목록에서 생성한 NFV Farm을 확인합니다.

### NFV Farm 수정

NFV Farm 정보를 수정하는 기능입니다.

> **참고.**
>
> NFV Farm을 사용하여 생성한 VNF가 있는 경우, 수정 할 수 없습니다.

1. 왼쪽 메뉴에서 'VNF 관리 > 기준정보 > NFV Farm' 를 클릭하여 NFV Farm 목록을 조회합니다.
2. 수정할 NFV Farm 선택 후, 좌측 상단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (203).png" alt=""><figcaption></figcaption></figure>

3. NFV Farm 수정 정보를 입력합니다. [NFV Farm 생성](nfv-farm.md#nfv-farm-1)을 참고하십시오.
4.  팝업창 우측 하단 수정 버튼을 클릭합니다.\\

    <figure><img src="../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>
5. NFV Farm 목록에서 수정한 NFV Farm 의 수정 사항을 확인합니다.

### NFV Farm 삭제

NFV Farm정보를 삭제하는 기능입니다.

> **참고.**
>
> NFV Farm을 사용하여 생성한 VNF가 있는 경우, 삭제 할 수 없습니다.

1. 왼쪽 메뉴에서 'VNF 관리 > 기준정보 > NFV Farm' 를 클릭하여 NFV Farm 목록을 조회합니다.
2. 삭제할 NFV Farm 선택 후, 좌측 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (204).png" alt=""><figcaption></figcaption></figure>

3. 팝업창 우측 하단 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (132).png" alt="" width="375"><figcaption></figcaption></figure>

4. NFV Farm 목록에서 NFV Farm 삭제 여부를 확인합니다.
