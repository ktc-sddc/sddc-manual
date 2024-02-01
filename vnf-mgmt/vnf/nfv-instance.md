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

# NFV Instance

***

## 개요

NS Package 파일을 기반으로 실제 NFV Instance를 생성 및 배포하는 기능을 제공합니다. NFV Instance 생성, 삭제와 활성화는 완료까지 수 분이 소요됩니다. 완료되면 우측 상단의 알림이 나타납니다.

> **참고**
>
> * 생성된 NFV Instance를 실제 네트워크에 연결하고, 사용하기 위해서 Instance 활성화를 필수적으로 진행해야 합니다.

> **주의**
>
> * Instance 활성화는 NS Package가 참조하고 있는 VNF Package의 HA 설정 유무에 따라 사용 가능한 License가 충분히 존재해야 합니다.

### NFV Instance 상태

<table><thead><tr><th width="230">NFV Instance 상태(영문)</th><th>NFV Instance 상태(한글)</th><th>설명</th></tr></thead><tbody><tr><td>BUILDING</td><td>생성중</td><td>NFV Instance를 생성 중입니다. 생성이 완료되기 전에 삭제를 진행할 수 있습니다.</td></tr><tr><td>READY</td><td>정상</td><td>NFV Instance 생성이 완료된 상태입니다. 활성화를 통해 네트워크 연결 및 VNF 기능을 사용할 수 있습니다.</td></tr><tr><td>TERMINATING</td><td>삭제중</td><td>NFV Instance 삭제 중입니다.</td></tr><tr><td>BROKEN</td><td>비정상</td><td>NFV Instance가 비정상 동작 중인 상태입니다.</td></tr></tbody></table>

### NFV Instance 활성화 상태

| 활성화 상태(영문)       | 활성화 상태(한글) | 설명                                                         |
| ---------------- | ---------- | ---------------------------------------------------------- |
| ACTIVATING       | 활성화 실행중    | NFV Instance를 활성화 중입니다. 활성화가 완료되기 전에 Instance를 삭제할 수 없습니다. |
| ACTIVATED        | 활성         | NFV Instance가 활성화가 완료된 상태입니다.                              |
| ACTIVATE\_FAILED | 실패         | NFV Instance 활성화가 실패한 상태입니다.                               |

## 사용 가이드

### NFV Instance 목록 조회

왼쪽 메뉴에서 VNF 관리 > VNF > NFV Instance 를 클릭하여 NFV Instance 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/image (179).png" alt=""><figcaption></figcaption></figure>

### NFV Instance 상세 조회

NFV Instance 목록 화면에서 특정 Instance를 선택하면 상세 정보를 확인할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

### NFV Instance 생성

1. 왼쪽 메뉴에서 VNF 관리 > VNF > NFV Instance 를 클릭합니다.
2. 상단의 생성 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure>

3. 팝업 창이 나타나면, NS Instance 생성 정보를 입력합니다.
   * NFV Instance 이름 : NFV Instance 이름을 입력합니다.
   * NS Package : NFV Instance로 생성할[ NS Package](ns-package.md)를 선택합니다.
   * NFV Farm : 배포할 [NFV Farm](../nfv-farm.md)을 선택합니다.
   * 할당할 Tenant / VPC 정보 : NFV Instance를 할당할 Tenant, [VPC](../../network/vpc.md)를 선택합니다.
   * NFV Interface 구성 : Interface 유형별 NFV Subnet을 선택합니다.
   * 설명 : NFV Instance에 대한 설명을 입력합니다.
4. 팝업창 우측 하단 생성 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

5. NFV Instance 목록에서 생성한 NFV Instance를 확인합니다.

### NFV Instance 활성화

1. 왼쪽 메뉴에서 VNF 관리 > VNF > NFV Instance 를 클릭합니다.
2. NFV Instance 목록에서 활성화하고자 하는 Instance를 선택 후, 상단의 Instance 활성화 버튼을 클릭합니다.

"이미지"

3. 팝업 창이 나타나면, 활성화하려는 Instance에 대한 정보를 재확인하고 활성화 버튼을 클릭합니다.

"이미지"

4. NFV Instance 목록에서 NFV Instance의 활성화 상태를 확인합니다.

### NFV Instance 삭제

1. 왼쪽 메뉴에서 VNF 관리 > VNF > NFV Instance 를 클릭합니다.
2. NFV Instance 목록에서 삭제하고자 하는 Instance를 선택 후, 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (181).png" alt=""><figcaption></figcaption></figure>

3. 팝업창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (160).png" alt="" width="375"><figcaption></figcaption></figure>

4. NFV Instance 목록에서 NFV Instance 삭제 여부를 확인합니다.

## FAQ

> **Q. Instance가 삭제 되지 않습니다.**
>
> A. 해당 Instance를 참조하고 있는 [Device](device.md)가 있을 경우, 해당 Device를 먼저 삭제하시고 다시 시도해주시기 바랍니다.

> **Q. 동일한 NS Package 파일을 참조하여 다른 Instance를 생성할 수 있습니까?**
>
> A. 네. 동일한 NS Package를 참조하여 서로 다른 Instance를 생성 및 배포할 수 있습니다.

> **Q. NFV Instance 상태가 Broken에서 바뀌지 않습니다.**
>
> A. 시스템 관리자(sddc.ktcloud@kt.com)에게 문의하시기 바랍니다.
