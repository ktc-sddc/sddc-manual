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

# Server Snapshot

***

## 개요

Server Snapshot 기능을 통해 Server에 대한 백업 및 복구를 지원합니다.

#### Server Snapshot 상태 정의

<table data-full-width="false"><thead><tr><th width="156">상태(영문)</th><th width="148">상태(한글)</th><th>설명</th></tr></thead><tbody><tr><td>ACTIVE</td><td>활성</td><td>Server Snapshot 이 정상 생성되었습니다.</td></tr><tr><td>ERROR</td><td>에러</td><td>Server Snapshot 생성이 실패하였습니다.</td></tr><tr><td>UNMANAGED</td><td>비정상</td><td>Server Snapshot 이 비상적인 상태로 관리자의 확인이 필요합니다.</td></tr></tbody></table>

## 사용 가이드

### Server Snapshot 목록 조회

Tenant 내에서 생성된 Server Snapshot 목록을 조회합니다.

1. Compute > Server Snapshot 메뉴를 클릭합니다.
2. Server Snapshot 목록을 확인합니다.

<figure><img src="../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure>

### Server Snapshot 상세 조회

1. Compute > Server Snapshot 메뉴를 클릭합니다.
2. Server Snapshot 목록정보를 확인합니다.
3. 조회할 Server Snapshot을 클릭합니다.

<figure><img src="../.gitbook/assets/image (425).png" alt=""><figcaption></figcaption></figure>

### Server Snapshot 생성

Server 백업을 위한 Server Snapshot을 생성합니다.

{% hint style="danger" %}
**주의**

실행 중인 Server에 대한 Snapshot을 생성할 수 있으나, 이 경우 일부 데이터가 손상될 수 있습니다.
{% endhint %}

1. Compute > Server 메뉴를 클릭합니다.
2. 목록 상단에 **\[스냅샷]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (422).png" alt=""><figcaption></figcaption></figure>

3. Snapshot 생성 팝업 창에서 정보를 입력한 후 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (423).png" alt="" width="375"><figcaption></figcaption></figure>

### Server Snapshot 수정

Server Snapshot을 수정합니다.

1. Compute > Server Snapshot 메뉴를 클릭합니다.
2. 대상 Server Snapshot을 선택한 다음 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (427).png" alt=""><figcaption></figcaption></figure>

3. 수정 팝업 창에서 수정할 정보(이름, 설명)를 입력하고 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (429).png" alt="" width="375"><figcaption></figcaption></figure>

### Server Snapshot 삭제

사용하지 않는 Server Snapshot을 삭제합니다.

{% hint style="danger" %}
**주의**

Server Snapshot 삭제 시 데이터 복구가 불가능합니다.
{% endhint %}

1. Compute > Server Snapshot 메뉴를 클릭합니다.
2. 대상 Server Snapshot을 선택한 다음 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (426).png" alt=""><figcaption></figcaption></figure>

3. 삭제 팝업 창에서 삭제 대상을 확인 후 **\[삭제]** 버튼을 클릭합니다.
   * 반납 보호된 Snapshot은 아래와 같이 이름을 입력한 후 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (428).png" alt="" width="375"><figcaption></figcaption></figure>

### Server 복원

{% hint style="info" %}
**참고**

* 원본 Server 및 Volume이 반드시 존재해야 합니다.
* OS Image의 경우 원본 Server 정보가 적용됩니다.
* 원본 Server에 연결된 추가 Volume이 존재할 경우, Server 복원 시에 추가 Volume도 함께 생성됩니다.
{% endhint %}

1. Compute > Server Snapshot 메뉴를 클릭합니다.
2. 대상 Server Snapshot을 선택하여 **\[SERVER 복원]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (430).png" alt=""><figcaption></figcaption></figure>

3. Server 복원에 필요한 **기본 사항** (Server 이름 / Flavor 종류 / Flavor 유형)을 입력 및 선택합니다.

<figure><img src="../.gitbook/assets/image (433).png" alt=""><figcaption></figcaption></figure>

4. **Server 설정 정보** (Network Interface)을 입력 및 선택합니다.

<figure><img src="../.gitbook/assets/image (434).png" alt=""><figcaption></figcaption></figure>

5. **추가 설정 정보** (반납보호 여부 / Key Pair / Init Script)를 입력 및 선택합니다.

<figure><img src="../.gitbook/assets/image (435).png" alt=""><figcaption></figcaption></figure>

6. 입력 정보를 **검토** 한 뒤, **\[복원]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (436).png" alt="" width="375"><figcaption></figcaption></figure>

7. Compute > Server 메뉴로 이동하여, 복원된 Server를 확인합니다.

<figure><img src="../.gitbook/assets/image (437).png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. 원본 데이터가 손상될 경우 어떻게 되나요?**
>
> **A.** Snapshot은 원본 데이터를 참조하기 때문에 Server 복원이 정상적으로 수행되지 않을 수 있습니다.
