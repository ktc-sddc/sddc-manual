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

# Server

***

## 개요

Server 자원에 대한 생성 및 삭제와 함께 시작/정지와 같은 동작 제어 기능을 제공합니다.

Server를 생성하기 위해서는 관련된 VPC, Subnet, Key Pair 등이 선행적으로 생성되어 있어야 합니다.

#### Server 상태 정의

<table><thead><tr><th width="153">상태(영문)</th><th width="119">상태(한글)</th><th width="585">설명</th></tr></thead><tbody><tr><td>BUILD</td><td>처리중</td><td>Server 생성 또는 정지 등의 요청 동작을 진행중인 상태입니다.</td></tr><tr><td>ACTIVE</td><td>운영중</td><td>Server가 실행 중인 상태로, Server 접근이 가능합니다.</td></tr><tr><td>SHUTOFF</td><td>정지됨</td><td>Server가 정지된 상태입니다.</td></tr><tr><td>ERROR</td><td>에러</td><td>생성 혹은 정지와 같은 동작 제어가 정상적으로 진행되지 않은 상태로, 관리자의 확인이 필요한 상태입니다.</td></tr><tr><td>UNMANAGED</td><td>비정상</td><td>Server가 정상적이지 않은 상태로 관리자의 확인이 필요한 상태입니다.</td></tr></tbody></table>

## 사용 가이드

### Server 목록 조회

선택한 Tenant에 생성된 Server 목록을 조회할 수 있습니다.

1. Compute > Server 메뉴를 클릭합니다.
2. Server 목록을 확인합니다.

<figure><img src="../.gitbook/assets/image (360).png" alt=""><figcaption></figcaption></figure>

### **Server 상세 보기**

Server 목록 화면에서 특정 Server를 선택하면 해당 Server의 상세정보를 확인할 수 있습니다.

1. Compute > Server 메뉴를 클릭합니다.
2. Server 목록을 확인합니다.
3. 조회 할 Server를 선택한 후 상세 내용을 확인합니다.

<figure><img src="../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

### Server 신규 생성

새로운 Server를 생성합니다.

{% hint style="info" %}
**참고**

* Server가 내외부 통신을 위해 필요한 Network Interface는 미리 생성하시기 바랍니다.
* Key Pair와 Init Script의 경우 미리 준비(생성) 혹은 Server 생성을 진행하면서 동시 생성도 가능합니다.
{% endhint %}

1. Compute > Server 메뉴를 클릭합니다.
2. 목록 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (362).png" alt=""><figcaption></figcaption></figure>

3. Server 생성과 관련된 **기본 정보**(Server 이름/ Server 상품 유형/ Flavor 종류 및 유형)를 입력 및 선택합니다.

<figure><img src="../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

4. Server 생성 시 사용할 이미지를 선택합니다.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

5.  **Server 설정** 정보(Volume 상품, Network Interface 등)를 선택합니다.\


    <figure><img src="../.gitbook/assets/image (736).png" alt=""><figcaption></figcaption></figure>
6.  **추가 설정** 정보(반납보호 선택 여부, Key Pair, Init Script)를 입력 및 선택합니다.\


    <figure><img src="../.gitbook/assets/image (738).png" alt=""><figcaption></figcaption></figure>
7.  입력 및 선택한 정보를 **검토** 한 뒤, **\[생성]** 버튼을 클릭합니다.\


    <figure><img src="../.gitbook/assets/image (368).png" alt="" width="375"><figcaption></figcaption></figure>
8. Server 생성 결과를 확인합니다.

### Server 동작 제어

시작, 정지, 재시작 등 Server의 상태를 제어할 수 있습니다.

**제공되는 동작**

<table><thead><tr><th width="167">Server 동작</th><th width="580">설명</th></tr></thead><tbody><tr><td>시작</td><td>Server를 시작합니다.</td></tr><tr><td>정지</td><td>Server를 정지합니다.</td></tr><tr><td>재시작</td><td>Server를 재시작합니다.</td></tr><tr><td>강제 재시작</td><td>Server를 강제로 재시작합니다.</td></tr></tbody></table>

**제어 절차**

1. Compute > Server 메뉴를 클릭합니다.
2. 제어하고자 하는 Server 를 선택합니다.
3. 목록 상단에 제어하고자 하는 동작을 선택합니다.
4. 동작이 수행 된 후, 정상적으로 수행되었는 지 Server 상태를 확인합니다.

<figure><img src="../.gitbook/assets/image (369).png" alt=""><figcaption></figcaption></figure>

### Server 삭제

사용하지 않는 Server를 삭제할 수 있습니다

{% hint style="danger" %}
**주의**

* Server Snapshot 이 존재할 경우 원본 Server 삭제가 불가능합니다. Server Snapshot을 먼저 제거한 후 Server 삭제를 진행하시기 바랍니다.
* 삭제한 Server는 복구가 불가합니다.
{% endhint %}

1. Compute > Server 메뉴를 클릭합니다.
2. 삭제할 Server를 선택하고 목록 상단에 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (370).png" alt=""><figcaption></figcaption></figure>

3. 삭제 팝업 창에서 대상을 확인하고 **\[삭제]** 버튼을 클릭합니다.
   * 반납 보호가 설정된 Server는 아래와 같이 절차를 진행한 뒤 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (371).png" alt="" width="375"><figcaption></figcaption></figure>

4. Server 목록 화면에서 삭제 Server가 조회되지 않는지 확인합니다.

### Server Terminal 접속

Server에 대해서 GUI 기반으로 직접 접속할 수 있는 기능을 제공합니다.

{% hint style="info" %}
**참고**

Server Terminal 생성 후 10분 간은 다른 사용자가 동일 Server에 대해서 Terminal 동시 접근이불가합니다.
{% endhint %}

1. Compute > Server 메뉴를 클릭합니다.
2. 접속할 Server를 선택하고 목록 상단에 **\[터미널]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (372).png" alt=""><figcaption></figcaption></figure>

3. Server Terminal 시작 팝업 창에서 대상 Server를 확인한 뒤 **\[시작]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (373).png" alt="" width="375"><figcaption></figcaption></figure>

4. 발급받은 터미널 탭으로 이동합니다.

<figure><img src="../.gitbook/assets/image (375).png" alt=""><figcaption></figcaption></figure>

### Server 로그

Server 의 최근 로그를 최대 10,000라인까지 조회할 수 있습니다.

1. Compute > Server 메뉴를 클릭합니다.
2. 대상 Server를 선택하고 목록 상단에 **\[로그]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (377).png" alt=""><figcaption></figcaption></figure>

3. 로그 팝업 창에서 라인 수를 변경하면 터미널 로그를 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (379).png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. Server생성 시 에러가 발생합니다.**
>
> A. 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.

> **Q. Server 생성 시 직접 CPU 나 Memory 설정이 가능한가요?**
>
> A. 제공되는 Flavor 타입 내에서만 Server 생성이 가능합니다.

> **Q. Server 생성 시 제공되는 이미지 외에 사용이 가능한가요?**
>
> A. 현재 제공되는 이미지로만 Server 생성이 가능합니다.\
> 추가 이미지 필요 시 시스템 관리자(sddc.ktcloud@kt.com)에게 문의하시기 바랍니다.

