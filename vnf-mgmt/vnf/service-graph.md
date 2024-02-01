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

# Service Graph

***

## 개요

Service Graph 는 vWAF, vFW 등 SDDC Platform에서 제공하는 [Device](device.md) 와 Routing 간 연결정보 관리합니다. Service Graph는 Routing을 제외한, 라우팅 Object (VPC Peering / Colocation Gateway 연결 / Cloud Connect 연결)에 연결하여 사용할 수 있습니다.

## 사용 가이드

### Service Graph 목록 조회

전체 Service Graph 목록을 조회하는 기능입니다.

왼쪽 메뉴에서 VNF 관리 > VNF > Service Graph 화면으로 이동합니다. \\

<figure><img src="../../.gitbook/assets/image (217).png" alt=""><figcaption></figcaption></figure>

### Service Graph 생성

Service Graph 를 생성하는 기능입니다.

1. 왼쪽 메뉴에서 VNF 관리 > VNF > Service Graph 화면으로 이동합니다.
2. 좌측 상단의 생성 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (218).png" alt=""><figcaption></figcaption></figure>

3. Service Graph 생성에 필요한 필수 정보를 입력합니다.
   * Service Graph 이름 : Service Graph의 이름입니다.
   * Tenant 이름 : 드롭다운 목록에서 해당 Service Graph를 사용할 Tenant를 선택합니다.
   * NFV Device 목록 : Service Graph로 구성할 Device를 드롭다운 목록에서 선택합니다.\
     \* 23년 7월 현재 Service Graph로 구성할 수 있는 네트워크 서비스는 vFW입니다.
4. 팝업창 우측 하단의 생성 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (219).png" alt=""><figcaption></figcaption></figure>

5. Serivce Graph 목록에서 생성한 Service Graph 를 확인합니다.

### Service Graph 삭제

Service Graph 를 삭제하는 기능입니다.

> **참고.**
>
> PBR 연결 중인 Service Graph 는 삭제가 불가능합니다.

1. 왼쪽 메뉴에서 VNF 관리 > VNF > Service Graph 화면으로 이동합니다.
2. 좌측 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (220).png" alt=""><figcaption></figcaption></figure>

3. 팝업창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (222).png" alt="" width="375"><figcaption></figcaption></figure>

4. Serivce Graph 목록에서 삭제한 Service Graph 를 확인합니다.

### PBR 등록

Service Graph 를 Routing 에 연결하는 기능입니다. PBR 등록이 되면 Routing 에 Service Graph 에 등록된 Device 기능이 적용됩니다.

1. 왼쪽 메뉴에서 VNF 관리 > VNF > Service Graph 화면으로 이동합니다.
2. 좌측 상단의 PBR 등록 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (221).png" alt=""><figcaption></figcaption></figure>

3. PBR 등록 정보를 입력합니다.
   * PBR 등록 대상 Route : Service Graph 를 연결하여 Device 기능을 적용할 Route 입니다.
4. 팝업창 우측 하단의 등록 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (223).png" alt=""><figcaption></figcaption></figure>

5. Service Graph 목록 화면에서 PBR 등록 정보를 확인합니다.

### PBR 해제

Routing 에 연결된 Service Graph 를 연결 해제하는 기능입니다. PBR이 해제 되면 Routing 에 Service Graph 에 등록된 Device 기능이 적용되지 않습니다.

1. 왼쪽 메뉴에서 VNF 관리 > VNF > Service Graph 화면으로 이동합니다.
2. 좌측 상단의 PBR 해제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (224).png" alt=""><figcaption></figcaption></figure>

3. 팝업창 우측 하단의 해제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (225).png" alt="" width="375"><figcaption></figcaption></figure>

4. Service Graph 목록 화면에서 PBR 등록 정보를 확인합니다.

## FAQ

> **Q. Service Graph 생성 시 Device 목록이 보이지 않습니다.**
>
> A. Device 생성 메뉴에서 Device를 사전에 생성해야 합니다. \\
>
> Q\*\*. Service Graph 로 구성할 수 있는 서비스는 무엇인가요?\*\*
>
> A.23년 7월 현재 Service Graph로 구성할 수 있는 네트워크 서비스는 vFW입니다.
