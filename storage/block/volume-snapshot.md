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

# Volume Snapshot

***

## 개요

Volume Snapshot 수정, 삭제, Volume 복원 기능을 통해 Volume에 대한 백업을 지원합니다.

## 사용 가이드

### Volume Snapshot 목록 조회

Tenant 내에서 사용 중인 Volume Snapshot 목록을 조회합니다.

1. Storage > Block Storage > Volume Snapshot 메뉴를 클릭합니다.
2. Volume Snapshot 목록 정보를 확인합니다.

<figure><img src="../../.gitbook/assets/image (630).png" alt=""><figcaption></figcaption></figure>

*   상태

    <table data-full-width="false"><thead><tr><th width="201.92771084337352">상태(영문)</th><th width="106">상태(한글)</th><th>설명</th></tr></thead><tbody><tr><td><strong>AVAILABLE</strong></td><td><strong>사용 가능</strong></td><td>정상적으로 생성된 Volume Snapshot이며, Volume 복원이 가능합니다.</td></tr><tr><td><strong>ERROR</strong></td><td><strong>에러</strong></td><td>Volume Snapshot 생성을 실패하였습니다.</td></tr><tr><td><strong>ERROR_DELETING</strong></td><td><strong>삭제 에러</strong></td><td>Volume Snapshot 삭제를 실패하였습니다.</td></tr></tbody></table>
* 크기: 원본 Volume의 크기

### Volume Snapshot 상세 조회

1. Storage > Block Storage > Volume Snapshot 메뉴를 클릭합니다.
2. Volume Snapshot 목록 정보를 확인합니다.
3. 조회할 Volume Snapshot을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (631).png" alt=""><figcaption></figcaption></figure>

### Volume Snapshot 생성

DATA Volume 백업을 위한 Volume Snapshot을 생성하는 기능입니다.

{% hint style="danger" %}
주의

* ROOT Volume에 대한 Volume Snapshot은 지원하지 않습니다.
* Volume이 서버에 연결된 상태에서 Volume Snapshot을 생성하면 일부 데이터가 손상될 수 있습니다.
{% endhint %}

1. Storage > Block Storage > Volume 메뉴를 클릭합니다.
2. 목록 상단에 **\[스냅샷 생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (627).png" alt=""><figcaption></figcaption></figure>

3. Snapshot 생성 팝업 창에서 정보를 입력한 후 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (628).png" alt="" width="340"><figcaption></figcaption></figure>



### Volume Snapshot 수정

생성된 Volume Snapshot의 정보를 수정합니다.

1. Storage > Block Storage > Volume Snapshot 메뉴를 클릭합니다.
2. 대상 Volume Snapshot을 선택하여 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (633).png" alt=""><figcaption></figcaption></figure>

3. 수정 팝업 창에서 입력 정보(Snapshot 이름 / 설명)를 수정한 후 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (632).png" alt="" width="340"><figcaption></figcaption></figure>

### Volume Snapshot 삭제

1. Storage > Block Storage > Volume Snapshot 메뉴를 클릭합니다.
2. 대상 Volume Snapshot을 선택하여 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (634).png" alt=""><figcaption></figcaption></figure>

3. 삭제 팝업 창에서 삭제 대상을 확인 후 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (635).png" alt="" width="342"><figcaption></figcaption></figure>

### Volume 복원

{% hint style="info" %}
참고

Volume Snapshot을 통한 Volume 복원 시 크기 및 상품 타입은 원본 Volume 정책을 따릅니다.
{% endhint %}

1. Storage > Block Storage > Volume Snapshot 메뉴를 클릭합니다.
2. 대상 Volume Snapshot을 선택하여 **\[VOLUME 복원]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (636).png" alt=""><figcaption></figcaption></figure>

3. 복원 팝업 창에서 정보를 입력한 후 **\[복원]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (637).png" alt="" width="344"><figcaption></figcaption></figure>

## FAQ

> **Q. Snapshot 상태가 ERROR\_DELETING 인 경우, 삭제가 불가능 하나요??**
>
> **A.** 네. 삭제가 불가능하며 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다
