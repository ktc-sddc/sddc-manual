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

# Init Script

***

## 개요

Server 생성 직후 초기 실행할 스크립트를 사전 작성 및 재사용 할 수 있도록 지원하는 기능입니다.

## 사용 가이드

### Init Script 목록 조회

Tenant 내에 등록되어 있는 Init Script 목록을 조회할 수 있습니다.

1. Compute > Init Script를 클릭합니다.
2. Init Script 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

### Init Script 생성

Init Script를 생성합니다.

{% hint style="info" %}
**참고**

* 현재 Linux만 지원합니다.
* Script 맨 첫 줄에 #/bin/bash, #/usr/bin/env python 과 같은 형태로 실행하려는 스크립트 경로를 반드시 입력하시기 바랍니다.
* 한글 및 주석은 입력이 불가능합니다.
* Script 자체의 오류 검증은 제공하지 않습니다.
{% endhint %}

1. Compute > Init Script를 클릭합니다.
2. 목록 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-05 오후 1.45.38 2.png" alt=""><figcaption></figcaption></figure>

1. 생성 팝업 창에서 필요한 정보를 입력하고 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (382).png" alt="" width="375"><figcaption></figcaption></figure>



### Init Script 수정

이미 생성된 Init Script를 수정합니다.

{% hint style="info" %}
**참고**

* Init Script의 수정 사항은 이미 생성된 Server에는 영향을 주지 않습니다.
{% endhint %}

1. Compute > Init Script를 클릭합니다.
2. 수정할 Init Script를 선택합니다.
3. 목록 상단에 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-05 오후 1.45.38 2 2 (1).png" alt=""><figcaption></figcaption></figure>

1. 수정 팝업 창에서 수정할 정보(이름, Script, 설명)를 입력하고 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (384).png" alt="" width="375"><figcaption></figcaption></figure>

### Init Script 삭제

사용하지 않을 Init Script를 삭제할 수 있습니다.

{% hint style="info" %}
**참고**

* Init Script를 삭제하더라도 기존 적용된 Server에 영향을 미치지 않습니다.
{% endhint %}

1. Compute > Init Script를 클릭합니다.
2. 삭제할 Init Script를 선택합니다.
3. 목록 상단에 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-05 오후 1.45.38.png" alt=""><figcaption></figcaption></figure>

4. 삭제 팝업 창에서 삭제 대상 정보를 확인 후 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/Screenshot 2024-02-05 at 14.39.53.png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. Server 생성 후 Init Script의 실행 결과는 어떻게 확인할 수 있나요?**
>
> **A.** Init Script 실행 결과는 Compute > Server 메뉴에서 생성한 Server를 선택한 후 터미널에 접속하거나 최근 로그 조회를 통해 확인할 수 있습니다.

> **Q. Init Script의 정상적으로 동작하지 않은 것 같습니다. 어떻게 해야 하나요?**
>
> **A.** Init Script 자체에 오류가 있는지 먼저 확인하시기 바랍니다. 만약 오류 수정이 필요한 경우 Server에 직접 접속하여 Init Script를 수정해야 합니다.
>
> Init Script의 오류가 없는데도 정상 동작하지 않은 경우는 시스템 관리자(sddc.ktcloud@kt.com)으로 문의하시기 바랍니다.
