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

<figure><img src="../../.gitbook/assets/image (612).png" alt=""><figcaption></figcaption></figure>

* Share 상태

<table data-full-width="false"><thead><tr><th width="159">상태(영문)</th><th width="117.72950819672133">상태(한글)</th><th>설명</th></tr></thead><tbody><tr><td><strong>AVAILABLE</strong></td><td>사용가능</td><td>정상적으로 생성되었습니다.</td></tr><tr><td><strong>ERROR</strong></td><td>장애</td><td>Share 생성을 실패하였습니다.</td></tr><tr><td><strong>CREATING</strong></td><td>생성중</td><td>Share 생성 중입니다.</td></tr><tr><td><strong>UNMANAGED</strong></td><td>비정상</td><td>관리되지 않은 상태이며, 관리자에게 문의가 필요합니다.</td></tr></tbody></table>

### Share 생성

Server에서 추가적으로 연결 가능한 Share을 생성할 수 있습니다.

{% hint style="info" %}
**참고**

Share은 최소 300GB부터 최대 1TB까지 지원합니다.
{% endhint %}

1. Storage > Share Storage > Share 메뉴로 이동합니다.
2. 목록 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 2.25.48.png" alt=""><figcaption></figcaption></figure>

3. 생성 팝업 창에서 정보를 입력한 후 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (613).png" alt=""><figcaption></figcaption></figure>

### Share 수정

생성된 Share 정보를 수정하는 기능입니다.

1. Storage > Share Storage > Share 메뉴를 클릭합니다.
2. 대상 Share을 선택하여 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 2.25.48 2.png" alt=""><figcaption></figcaption></figure>

3. 수정 팝업 창에서 입력 정보를 수정한 후 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (614).png" alt=""><figcaption></figcaption></figure>

### Share 삭제

Share을 삭제하는 기능입니다.

1. Storage > Share Storage > Share 메뉴를 클릭합니다.
2. 대상 Share을 선택하여 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 2.25.48 3.png" alt=""><figcaption></figcaption></figure>

3. 삭제 팝업 창에서 삭제 대상을 확인 후 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (615).png" alt=""><figcaption></figcaption></figure>

### Share 마운트

#### 마운트 경로 확인

Server에 추가 Share을 연결하는 기능입니다.\
대상 Server에 접속하여 마운트 작업을 수행해야 사용이 가능합니다.

1. Storage > Share Storage > Share 메뉴를 클릭합니다.
2. Mount Path 를 확인합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 2.30.20 (2).png" alt=""><figcaption></figcaption></figure>

#### Server에 마운트 하기

연결된 Share 를 사용하기 위해서는 Server 콘솔을 통하여 Mount 과정을 거쳐야 합니다.

1. Compute > Server 메뉴를 클릭합니다.
2. 대상 Server를 선택하여 **\[터미널]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (542).png" alt=""><figcaption></figcaption></figure>

3. 마운트 경로를 생성하고, 해당 Share를 경로에 마운트 합니다.

```
$ mkdir /mnt/share
$ mount -t nfs {mount path} /mnt/share
$ df -h
```

#### **서버 마운트 해제**

Server로부터 Share의 마운트를 해제하는 기능입니다

1. Server 콘솔에서 Mount된 Share을 Unmount 합니다.

```
$ umount /mnt/share
$ df -h
```

## FAQ

> **Q. 최대 용량(1TB)을 초과하여 생성이 필요한 경우에는 어떻게 해야하나요?**
>
> **A.** 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
