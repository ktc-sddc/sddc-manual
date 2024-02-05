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

# Share

## 개요

Share 생성, 수정, 삭제, 동작 제어 등을 제공하는 기능입니다.

해당 Tenant 내의 Server에 mount Path를 통해 마운트하여 사용할 수 있습니다.

## 사용 가이드

### Share 목록 조회

Tenant 내에서 사용 중인 Share 목록을 조회합니다.

1. Storage > Share Storage > Share 메뉴를 클릭합니다.
2. Share 목록 정보를 확인합니다.

<figure><img src="../../.gitbook/assets/image (530).png" alt=""><figcaption><p>&#x3C;Block Storage Volume 조회화면></p></figcaption></figure>

* Share 상태

<table data-full-width="false"><thead><tr><th width="159">상태(영문)</th><th width="117.72950819672133">상태(한글)</th><th>설명</th></tr></thead><tbody><tr><td><strong>AVAILABLE</strong></td><td>사용가능</td><td>Server 에 연결이 가능한 상태입니다.</td></tr><tr><td><strong>IN-USE</strong></td><td>사용중</td><td>Server 에 연결된 상태입니다.</td></tr><tr><td><strong>ERROR</strong></td><td>장애</td><td>Volume 생성을 실패하였습니다.</td></tr><tr><td><strong>CREATING</strong></td><td>처리중</td><td>Volume 생성 중입니다.</td></tr><tr><td><strong>ATTACHING</strong></td><td>처리중</td><td>Volume을 Server에 연결 중입니다.</td></tr><tr><td><strong>DETACHING</strong></td><td>처리중</td><td>Server 에서 Volume 연결을 해제하는 중입니다.</td></tr><tr><td><strong>EXTENDING</strong></td><td>처리중</td><td>Volume Size를 확장하고 있습니다.</td></tr><tr><td><strong>UNMANAGED</strong></td><td>비정상</td><td>관리되지 않은 상태이며, 관리자에게 문의가 필요합니다.</td></tr></tbody></table>

### Volume 상세 보기

Volume 목록 화면에서 특정 Volume을 선택하면 상세 정보를 확인할 수 있습니다.

* **연결된 Server 정보: 연결된 서버명과 디바이스명**\
  연결된 Server가 없으면 "연결된 Server가 존재하지 않습니다."라고 보여집니다.
* **연결된 Server Snapshot 정보: 연결된 Server를 통해 생성한 Server Snapshot 정보**\
  연결된 Server Snapshot이 없으면 "연결된 Server Snapshot이 존재하지 않습니다."라고 보여줍니다.
*   **연결된 Volume Snapshot 정보: 해당 Volume을 통해 생성한 Snapshot 정보**

    하나의 Volume은 1개 이상의 Volume Snapshot을 생성할 수 있으며, 생성된 Volume Snapshot이 없으면 "연결된 Volume Snapshot이 존재하지 않습니다."라고 보여줍니다.

<figure><img src="../../.gitbook/assets/image (462).png" alt=""><figcaption></figcaption></figure>

### Volume 생성

Server에서 추가적으로 연결 가능한 DATA Volume을 생성할 수 있습니다..

{% hint style="info" %}
**참고**

DATA Volume은 최소 10GB부터 최대 1TB까지 지원합니다.
{% endhint %}

1. Storage > Block Storage > Volume 메뉴로 이동합니다.
2. 목록 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (532).png" alt=""><figcaption></figcaption></figure>

1.  생성 팝업 창에서 정보를 입력한 후 **\[생성]** 버튼을 클릭합니다.

    <figure><img src="../../.gitbook/assets/image (533).png" alt="" width="338"><figcaption></figcaption></figure>

* Volume 상품
  * HDD
  * SSD(출시 예정)

### Volume 수정

생성된 Volume 정보를 수정하는 기능입니다.

1. Storage > Block Storage > Volume 메뉴를 클릭합니다.
2. 대상 Volume을 선택하여 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (534).png" alt=""><figcaption></figcaption></figure>

1. 수정 팝업 창에서 입력 정보(Storage 이름 / 설명 / 반납보호 여부)를 수정한 후 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (535).png" alt=""><figcaption></figcaption></figure>

### Volume 삭제

필요 없는 Volume을 삭제하는 기능입니다.

{% hint style="info" %}
**참고**

* ROOT 타입의 Volume은 삭제할 수 없으며, Server 삭제 시 함께 삭제됩니다.
* Server에 연결되어 있는 Volume은 삭제할 수 없으며, 먼저 Server 연결을 해제해야 합니다.
* 연관된 Server Snapshot 또는 Volume Snapshot이 존재할 경우 삭제할 수 없으며, 먼저 관련된 Snapshot을 삭제해야 합니다.
* 한번 삭제된 Volume의 데이터는 복구가 불가능합니다.
{% endhint %}

1. Storage > Block Storage > Volume 메뉴를 클릭합니다.
2. 대상 Volume을 선택하여 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (538).png" alt=""><figcaption></figcaption></figure>

1.  삭제 팝업 창에서 삭제 대상을 확인 후 **\[삭제]** 버튼을 클릭합니다.

    <figure><img src="../../.gitbook/assets/image (536).png" alt=""><figcaption></figcaption></figure>

### Volume 연결/해제

#### **서버에 연결**

Server에 추가 Volume을 연결하는 기능입니다.\
Volume을 Server에 연결한 후 대상 서버에 접속하여 Volume 마운트 작업을 수행해야 사용이 가능합니다.

1. Storage > Block Storage > Volume 메뉴를 클릭합니다.
2. 대상 Volume을 선택하여 **\[연결]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (539).png" alt=""><figcaption></figcaption></figure>

1.  Server 연결 팝업 창에서 연결 대상 Server를 선택한 후 **\[연결]** 버튼을 클릭합니다.

    <figure><img src="../../.gitbook/assets/image (537).png" alt=""><figcaption></figcaption></figure>

#### **연결된 볼륨 사용하기**

리눅스 서버의 경우 연결된 Volume을 사용하기 위해서는 Server 콘솔을 통하여 Mount 과정을 거쳐야 합니다.

1. Compute > Server 메뉴를 클릭합니다.
2. 대상 Server를 선택하여 **\[터미널]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (542).png" alt=""><figcaption></figcaption></figure>

3. Server 콘솔에서 연결된 Volume 정보를 확인합니다.

<figure><img src="../../.gitbook/assets/image (547).png" alt=""><figcaption></figcaption></figure>

4. Mount 위치를 생성하고, 연결된 Volume에 대해 포맷 및 파일시스템 생성 후 Mount 작업을 수행합니다.

<figure><img src="../../.gitbook/assets/image (546).png" alt=""><figcaption></figcaption></figure>

5. (옵션) 추가로 Mount된 Volume에 대해 Server 부팅 시 자동 Mount 설정을 추가하기 위하여 /etc/fstab에 추가합니다.

<figure><img src="../../.gitbook/assets/image (548).png" alt=""><figcaption></figcaption></figure>

#### **서버 연결 해제**

Server로부터 Volume을 연결 해제하는 기능입니다.

{% hint style="danger" %}
**주의**

* ROOT Volume은 서버 연결 해제가 불가능합니다.
* Server 실행 중에 해제가 가능하지만, 마운트된 상태로 해제할 경우 일부 데이터가 손상될 수 있습니다.
{% endhint %}

1. Server 콘솔에서 Mount된 Volume을 Unmount 합니다.

<figure><img src="../../.gitbook/assets/image (549).png" alt=""><figcaption></figcaption></figure>

2. Storage > Block Storage > Volume 메뉴를 클릭합니다.
3. 대상 Volume을 선택하여 **\[해제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (540).png" alt=""><figcaption></figcaption></figure>

3. Server 연결 해제 팝업 창에서 해제 대상을 확인한 후 **\[연결 해제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (541).png" alt=""><figcaption></figcaption></figure>

### **Volume 크기 확장**

Volume의 크기를 확장하는 기능입니다.\
Volume 연결 시와 동일하게 확장 후 대상 Server에 접속하여 파트션 작업 및 마운트 작업을 수행해야 합니다.

{% hint style="danger" %}
**주의**

* Server에 연결된 Volume은 크기를 확장할 수 없습니다. 먼저 Server 연결 해제가 필요합니다.
* 최대 1TB까지만 확장이 가능합니다. 이를 초과할 경우에는 새로운 Volume을 생성해야 합니다.
* Snapshot이 존재할 때 원본 볼륨을 확장하게 되면 Snapshot이 손상될 수 있습니다.
{% endhint %}

1. Storage > Block Storage > Volume 메뉴를 클릭합니다.
2. 대상 Volume을 선택하여 **\[확장]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (550).png" alt=""><figcaption></figcaption></figure>

3. 확장 팝업 창에서 원하는 크기를 입력한 후 **\[확장]** 버튼을 클릭합니다. 이 때, 입력된 크기가 최종 Volume 크기가 됩니다.

<figure><img src="../../.gitbook/assets/image (551).png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. 최대 용량(1TB)을 초과하는 경우에는 어떻게 해야하나요?**
>
> **A.** 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
