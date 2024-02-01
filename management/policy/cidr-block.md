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

# CIDR 관리

***

## 개요

CIDR Block 은 SDDC Platform 내에서 사용 가능한 CIDR 을 관리하여 서비스간 주소 범위 중복으로 발생할 수 있는 문제를 방지하는 기능입니다.

#### CIDR Block 유형

<table><thead><tr><th width="259.77097505668934">CIDR Block 유형</th><th>설명</th></tr></thead><tbody><tr><td>USER VPC</td><td>사용자 VPC 생성에 제공되는 CIDR Block</td></tr><tr><td>NFV</td><td>NFV 네트워크 자원 생성 시 사용되는 CIDR Block</td></tr><tr><td>default User VPC</td><td><a data-mention href="../../tenant-member.md#tenant">#tenant</a> 과정 중 default VPC 생성 시 사용되는 CIDR Block</td></tr><tr><td>default System VPC</td><td>System VPC 생성 시 사용되는 CIDR Block</td></tr><tr><td>default User Subnet</td><td><a data-mention href="../../tenant-member.md#tenant">#tenant</a> 과정 중 default Subnet 생성 시 사용되는 CIDR Block</td></tr><tr><td>default NAS Subnet</td><td><a data-mention href="../../storage/shared-storage-new/">shared-storage-new</a> 생성 시 사용되는 CIDR Block</td></tr></tbody></table>

## 사용 가이드

### CIDR Block 목록 조회

전체 CIDR Block 을 조회하는 기능입니다.

메뉴에서 시스템 관리 > 운영 정책 관리 > CIDR 관리 를 클릭하여 CIDR Block 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-01 오후 6.01.53.png" alt=""><figcaption></figcaption></figure>

### CIDR Block 생성

CIDR Block 을 생성하는 기능입니다.

{% hint style="info" %}
참고

* CIDR Block은 [유형](cidr-block.md#cidr-block)에 따라 플랫폼 내 특수한 목적으로 사용되며, 정책을 통해 사용 가능 혹은 불가능 여부가 결정할 수 있습니다.
* CIDR Block 사용 시, IP 주소 범위 중 Min 및 Max Mask 크기 내에서 사용될 수 있습니다.
* 동일한 유형의 CIDR 는 최대 1개 생성 가능합니다.
{% endhint %}

1. 메뉴에서 시스템 관리 > 운영 정책 관리 > CIDR 관리 를 클릭하여 CIDR Block 목록을 조회합니다.
2. 목록 상단에서 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.48.46.png" alt=""><figcaption></figcaption></figure>

3. 생성 팝업 창에서 정보를 입력 및 선택합니다.
   * 정책을 선택합니다. ALLOW 는 사용 가능, DENY 는 사용 불가능을 의미합니다.
   * CIDR Block 유형을 선택합니다. [CIDR Block 유형](cidr-block.md#cidr-block)에 따라 특수한 목적으로 사용됩니다.
   * IP 주소 범위를 입력합니다. CIDR Block 사용 시, 가능한 IP 주소 범위를 의미합니다.
   * Min Mask 를 입력합니다. CIDR Block 사용 시, 가능한 최소 크기의 IP 주소 범위 크기를 의미합니다.
   * Max Mask 를 입력합니다. CIDR Block 사용 시, 가능한 최대 크기의 IP 주소 범위 크기를 의미합니다.
   * 설명을 입력합니다.
4. **\[생성]** 버튼을 클릭 합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.48.59.png" alt=""><figcaption></figcaption></figure>

5. CIDR Block 목록에서 조회되는지 확인합니다.

### CIDR Block 삭제

CIDR Block 을 삭제하는 기능입니다.

1. 메뉴에서 시스템 관리 > 운영 정책 관리 > CIDR 관리를 클릭하여 CIDR Block 목록을 조회합니다.
2. 화면에서 삭제 할 CIDR Block 을 선택 후 목록 상단에서 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.49.22.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-01-31 오후 1.49.31.png" alt=""><figcaption></figcaption></figure>

4. CIDR Block 목록에서 삭제 되었는지 확인합니다.

## FAQ

> **Q. 동일한 유형의 CIDR 를 2개 이상 생성할 수 있나요?**
>
> A. 동일한 유형의 CIDR 는 최대 1개 생성 가능합니다.
