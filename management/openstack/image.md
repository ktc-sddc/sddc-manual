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

# Image 관리

***

## 개요

Server 생성 시 활용할 수 있는 Image 목록을 관리합니다.

OpenStack으로부터 Image 목록을 동기화 하여 SDDC Platform 사용자에게 서비스할 Image를 관리합니다.

### 제공 Image 목록(상용 기준 업데이트 예정)

<table><thead><tr><th width="355.73003581868903">Image 명</th><th width="183">OS</th><th>비고</th></tr></thead><tbody><tr><td>ipc-golden-centos74-ca-20230627</td><td>CentOs 7.4</td><td></td></tr><tr><td>ipc-golden-ubuntu2004-ca-20230627</td><td>Ubunut2004</td><td></td></tr><tr><td>ipc-golden-rocky86-ca-20230627</td><td>Rocky Linux 8.6</td><td></td></tr><tr><td>ipc-golden-redhat74-ca-20230627</td><td>RHEL 7.4</td><td>라이선스 필요</td></tr><tr><td>ipc-golden-redhat84-ca-20230627</td><td>RHEL 8.4</td><td>라이선스 필요</td></tr></tbody></table>



## 관리자 가이드

### Image 목록 조회

1. 시스템 관리 > OpenStack 관리 > Image 관리 메뉴를 클릭합니다.
2. 플랫폼에서 사용 가능한 Image 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/image (744).png" alt=""><figcaption></figcaption></figure>

### Image 관리하기

OpenStack과 동기화된 Image 목록 중 사용자에게 서비스 할 Image를 제어하는 기능을 제공합니다.

{% hint style="info" %}
**참고**

* 관리대상 여부에 따라 사용자 Server 생성 시 해당 Image 노출 여부가 결정됩니다.
{% endhint %}

{% hint style="danger" %}
**주의**

* Image를 사용하기 위해서 관련된 **속성 값(min\_ram, min\_disk, os\_version, os\_distro, disk\_format, CIM\_PASD\_InstructionSet, visibility="public")**들이 OpenStack에서 제대로 정의되었는지 확인해야 합니다.
{% endhint %}

1. 관리자 기능 > OpenStack 관리 > Image 관리 메뉴를 클릭합니다.
2. 변경할 Image를 선택 후 상단에 **\[설정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (746).png" alt=""><figcaption></figcaption></figure>

3. Image 관리 팝업 창에서 **\[해지]** 또는 **\[설정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (307).png" alt="" width="375"><figcaption></figcaption></figure>

### 신규 Image 추가하기

SDDC Platform에서 사용할 Image를 새로 추가할 수 있습니다. 이를 위해서는 OpenStack 관리자를 통해 신규 Image 업로드 및 메타 데이터 설정 등이 필요합니다.

{% hint style="danger" %}
**주의**

* 해당 작업은 OpenStack Dashboard -> SDDC Platform순으로 수행합니다.
* 사전 작업으로 OpenStack 내 실제 Image 는 사전 업로드 되어 있어야 합니다.
* 최소 디스크가 제대로 설정되지 않을 경우, 서버 생성 시 에러가 발생할 수 있습니다.
{% endhint %}

1. **\[OpenStack Dashboard]** Image 속성값 설정

<table><thead><tr><th width="147.5008872763442">속성명</th><th width="126">값</th><th>설명</th></tr></thead><tbody><tr><td>이미지 공유(visibility)</td><td>공용(public)</td><td>Image 공유 범위를 의미하며, 모든 테넌트에서 사용하기 위해서는 <strong>"공용"</strong>으로 설정이 필요하다.</td></tr><tr><td>최소 디스크(min_disk)</td><td></td><td>이미지 부팅을 위한 최소한의 디스크 공간이며, ROOT Volume 생성을 위한 필수 속성이다.</td></tr></tbody></table>

2. **\[OpenStack Dashboard]** Image 메타데이터 설정

<table><thead><tr><th width="198.5008872763442">필드명</th><th width="111">내용</th><th>설명</th></tr></thead><tbody><tr><td>USE_SDDC</td><td>true</td><td>SDDC 플랫폼 사용 여부를 표기합니다.</td></tr></tbody></table>

3. **\[SDDC Platform]** 관리자 기능 > OpenStack 관리 > Image 관리 메뉴를 클릭합니다.
4. **\[SDDC Platform]** 상단에 **\[동기화]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (745).png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. 생성하고자 하는 OS Image가 없습니다. 추가 가능한지요?**
>
> **A.** 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
