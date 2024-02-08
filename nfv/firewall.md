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

# 방화벽

***

## 개요

방화벽 서비스는 네트워크에서 발생하는 트래픽을 제어하는 기능을 제공하는 네트워크 보안 서비스입니다. 두 가지 유형의 방화벽을 제공하며, 네트워크 연결 유형에 따라 용도가 구분됩니다.

### 방화벽 유형

<table><thead><tr><th width="161">방화벽 유형</th><th>설명</th></tr></thead><tbody><tr><td>Inner FW</td><td>Tenant 내부 네트워크 통신 간 트래픽 제어에 사용되며, VPC Peering 에 적용할 수 있습니다.</td></tr><tr><td>Outer FW</td><td>Tenant 내부 네트워크와 외부 네트워크 통신 간 트래픽 제어에 사용되며, Colocation Gateway 연결과 Internet Gateway 연결에 적용할 수 있습니다.</td></tr></tbody></table>

## 사용가이드

### 방화벽 조회

현재 선택된 Tenant 에 생성된 방화벽을 조회하는 기능입니다.

메뉴에서 Security > 방화벽 을 클릭하여 방화벽 목록을 조회합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 2.57.11.png" alt=""><figcaption></figcaption></figure>

### 방화벽 생성

Tenant 에서 사용할 방화벽을 생성하는 기능입니다.

{% hint style="warning" %}
방화벽을 적용하고자 하는 네트워크 연결 유형을 고려하여 방화벽을 생성해야 합니다.

* Inner FW : VPC Peering
* Outer FW : Colocation Gateway 연결, Internet Gateway 연결
{% endhint %}

1. 메뉴에서 Security > 방화벽 메뉴를 클릭합니다.
2. 목록 상단에서 **\[방화벽 생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 2.57.56.png" alt=""><figcaption></figcaption></figure>

3. 방화벽 유형을 선택한 후 우측 하단 **\[다음]** 버튼을 클릭합니다.
   * Inner FW : VPC Peering 에 적용할 수 있는 방화벽입니다.
   * Outer FW : Colocation Gateawy 연결 또는 Internet Gateway 연결 에 적용할 수 있는 방화벽입니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.33.12.png" alt=""><figcaption></figcaption></figure>

4. 네트워크 환경에 맞는 방화벽 상품을 선택한 후, **\[다음]** 버튼을 클릭합니다
   * 방화벽 유형: Inner FW 혹은 Outer FW 를 의미합니다.
   * 이중화 : 방화벽 기능을 수행할 인스턴스가 이중화 구성됨을 의미합니다.
   * 사양 : 방화벽 기능을 수행할 인스턴스 사양을 의미합니다.&#x20;

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.33.26.png" alt=""><figcaption></figcaption></figure>

5. 정보를 입력한 후 **\[생성]** 버튼을 클릭합니다.
   * 방화벽 이름: 생성할 방화벽의 이름을 입력합니다.
   * 설명 : 생성할 방화벽의 설명을 입력합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.33.39.png" alt=""><figcaption></figcaption></figure>

6. 방화벽 메뉴에서 생성된 방화벽 상품을 확인합니다

### 방화벽 삭제

1. 메뉴에서 Security > 방화벽 메뉴를 클릭합니다.
2. 화면에서 삭제할 방화벽을 선택한 후 목록 상단 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.52.26.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.52.36.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, 방화벽 목록에서 삭제된 것을 확인할 수 있습니다.

### Inner FW 방화벽 연결 생성

1. 메뉴에서 Security > 방화벽 메뉴를 클릭합니다.
2. 화면에서 방화벽 연결을 생성할 Inner FW 유형 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 3.16.10.png" alt=""><figcaption></figcaption></figure>

3. 방화벽이 생성될 VPC 를 선택합니다.
4. 방화벽을 적용할 라우팅 리소스를 선택한 후 **\[추가]** 버튼을 클릭합니다. 화면 우측 미리보기를 통해 네트워크 구간 내 방화벽 적용 형상을 확인할 수 있습니다.
   * 라우팅 리소스 유형 : VPC Peering 으로 고정됩니다.
   * VPC Peering 이름 : 방화벽이 생성될 VPC 가 연결된 VPC Peering 목록이 조회됩니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.47.03.png" alt=""><figcaption></figcaption></figure>

5. 방화벽 우회 옵션을 선택합니다.
   * 허용 : 방화벽 인스턴스가 중단되었을 경우, 트래픽을 우회하여 라우팅 서비스가 유지되도록 합니다.
   * 거부 : 방화벽 인스턴스가 중단되었을 경우, 라우팅 서비스가 중단되도록 합니다.
6. 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.47.15.png" alt=""><figcaption></figcaption></figure>

7. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.05.49.png" alt=""><figcaption></figcaption></figure>

8. 팝업 창이 닫히고, 방화벽 목록이 조회됩니다. 방화벽 연결을 생성한 방화벽의 **\[방화벽 연결]** 버튼을 클릭하여 정보를 조회할 수 있습니다.

### Inner FW 방화벽 연결 > 라우팅 리소스 조회

메뉴에서 Security > 방화벽 메뉴를 클릭 후 조회할 Inner FW 유형 방화벽의 **\[방화벽 연결]** 버튼을 클릭하여 라우팅 리소스 목록을 조회합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.09.28.png" alt=""><figcaption></figcaption></figure>

### Inner FW 방화벽 연결 > 라우팅 리소스 수정

1. 메뉴에서 Security > 방화벽 메뉴를 클릭 후 조회할 Inner FW 유형 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다.
2. 라우팅 리소스 목록 상단 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.14.24.png" alt=""><figcaption></figcaption></figure>

3. 방화벽을 적용할 라우팅 리소스를 선택한 후 **\[추가]** 버튼을 클릭합니다. 화면 우측 미리보기를 통해 네트워크 구간 내 방화벽 적용 형상을 확인할 수 있습니다.
   * 라우팅 리소스 유형 : VPC Peering 으로 고정됩니다.
   * VPC Peering 이름 : 방화벽이 생성될 VPC 가 연결된 VPC Peering 목록이 조회됩니다.
4. 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.46.13.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.18.54.png" alt=""><figcaption></figcaption></figure>

6. 팝업 창이 닫히고, 라우팅 리소스 목록이 조회됩니다. 수정된 정보를 확인할 수 있습니다.

### Inner FW 방화벽 연결 > 라우팅 리소스 삭제

1. 메뉴에서 Security > 방화벽 메뉴를 클릭 후 조회할 Inner FW 유형 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다.
2. 삭제할 라우팅 리소스를 선택한 후 목록 상단 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.15.06.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.46.41.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, 라우팅 리소스 목록에서 삭제된 것을 확인할 수 있습니다.

### Inner FW 방화벽 연결 삭제

{% hint style="info" %}
**참고.**

* 방화벽 연결에 등록된 라우팅 리소스가 있다면 삭제할 수 없습니다.
{% endhint %}

1. 메뉴에서 Security > 방화벽 메뉴를 클릭 후 조회할 Inner FW 유형 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다.
2. 화면 상단 **\[방화벽 연결 삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.25.11.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 4.21.59.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, 방화벽 목록이 조회됩니다. 방화벽 연결을 삭제한 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다. 방화벽 연결 생성 화면으로 이동되면 삭제된 것을 확인할 수 있습니다.

### Outer FW 방화벽 연결 생성

{% hint style="info" %}
**참고.**

* Outer FW 방화벽 연결에는 1 개의 라우팅 리소스만 등록 가능합니다.
{% endhint %}

1. 메뉴에서 Security > 방화벽 메뉴를 클릭합니다.
2. 화면에서 방화벽 연결을 생성할 Outer FW 유형 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.03.48.png" alt=""><figcaption></figcaption></figure>

3. 방화벽을 적용할 라우팅 리소스를 선택한 후 **\[추가]** 버튼을 클릭합니다. 화면 우측 미리보기를 통해 네트워크 구간 내 방화벽 적용 형상을 확인할 수 있습니다.
   * 라우팅 리소스 유형 : Colocation Gateway 또는 Internet Gateway 를 선택할 수 있습니다.
   * 리소스 이름 : Tenant 내 Colocation Gateway 또는 Internet Gateway 가 조회됩니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.05.03.png" alt=""><figcaption></figcaption></figure>

4. 방화벽 우회 옵션을 선택합니다.
   * 허용 : 방화벽 인스턴스가 중단되었을 경우, 트래픽을 우회하여 라우팅 서비스가 유지되도록 합니다.
   * 거부 : 방화벽 인스턴스가 중단되었을 경우, 라우팅 서비스가 중단되도록 합니다.
5. 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.05.23.png" alt=""><figcaption></figcaption></figure>

6. 팝업 창 우측 하단의 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.05.49 (1).png" alt=""><figcaption></figcaption></figure>

7. 팝업 창이 닫히고, 방화벽 목록이 조회됩니다. 방화벽 연결을 생성한 방화벽의 **\[방화벽 연결]** 버튼을 클릭하여 정보를 조회할 수 있습니다.

### Outer FW 방화벽 연결 > 라우팅 리소스 조회

메뉴에서 Security > 방화벽 메뉴를 클릭 후 조회할 Outer FW 유형 방화벽의 **\[방화벽 연결]** 버튼을 클릭하여 라우팅 리소스 목록을 조회합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.16.53.png" alt=""><figcaption></figcaption></figure>

### Outer FW 방화벽 연결 > 라우팅 리소스 수정

1. 메뉴에서 Security > 방화벽 메뉴를 클릭 후 조회할 Outer FW 유형 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다.
2. 라우팅 리소스 목록 상단 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.17.47.png" alt=""><figcaption></figcaption></figure>

3. 방화벽을 적용할 라우팅 리소스를 선택한 후 **\[추가]** 버튼을 클릭합니다. 화면 우측 미리보기를 통해 네트워크 구간 내 방화벽 적용 형상을 확인할 수 있습니다.
   * 라우팅 리소스 유형 : Colocation Gateway 또는 Internet Gateway 를 선택할 수 있습니다.
   * 리소스 이름 : Tenant 내 Colocation Gateway 또는 Internet Gateway 가 조회됩니다.
4. 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.18.03.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.18.54 (1).png" alt=""><figcaption></figcaption></figure>

6. 팝업 창이 닫히고, 라우팅 리소스 목록이 조회됩니다. 수정된 정보를 확인할 수 있습니다.

### Outer FW 방화벽 연결 삭제

1. 메뉴에서 Security > 방화벽 메뉴를 클릭 후 조회할 Inner FW 유형 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다.
2. 화면 상단 **\[방화벽 연결 삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.24.12.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.24.21.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, 방화벽 목록이 조회됩니다. 방화벽 연결을 삭제한 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다. 방화벽 연결 생성 화면으로 이동되면 삭제된 것을 확인할 수 있습니다.

### 방화벽 정책 조회

메뉴에서 Security > 방화벽 메뉴를 클릭 후 정책을 조회할 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다. 방화벽 정책 탭을 클릭하여 정책 목록을 조회합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.27.47.png" alt=""><figcaption></figcaption></figure>

### 방화벽 정책 생성

1. 메뉴에서 Security > 방화벽 메뉴를 클릭 후 정책을 조회할 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다. 방화벽 정책 탭을 클릭합니다.
2. 목록 상단 **\[정책 관리]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.30.29.png" alt=""><figcaption></figcaption></figure>

3. 목록 상단 **\[+ 정책 추가]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.30.42.png" alt=""><figcaption></figcaption></figure>

4. 정책 정보를 입력합니다.
   1. <mark style="color:red;">**상세 가이드 필요**</mark>
5. **\[추가]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.31.00.png" alt=""><figcaption></figcaption></figure>

6. 목록에서 생성된 정책을 확인할 수 있습니다.

### 방화벽 정책 우선순위 변경

1. 메뉴에서 Security > 방화벽 메뉴를 클릭 후 정책을 조회할 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다. 방화벽 정책 탭을 클릭합니다.
2. 목록 상단 **\[정책 관리]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.41.18.png" alt=""><figcaption></figcaption></figure>

3. 우선순위를 변경할 정책을 선택한 후 목록 상단 **\[정책 이동]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.41.31.png" alt=""><figcaption></figcaption></figure>

4. 이동할 위치 정보를 입력합니다.
   * 정책 이름 : 이동 위치 기준이 되는 정책 이름을 선택합니다.
   * 위 혹은 아래 : 이동 위치 기준이 되는 정책의 바로 위 혹은 아래 이동 여부를 선택합니다.
5. **\[변경]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.41.46.png" alt=""><figcaption></figcaption></figure>

6. 목록에서 변경된 사항을 확인할 수 있습니다.

### 방화벽 정책 삭제

1. 메뉴에서 Security > 방화벽 메뉴를 클릭 후 정책을 조회할 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다. 방화벽 정책 탭을 클릭합니다.
2. 목록 상단 **\[정책 관리]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.41.18 (1).png" alt=""><figcaption></figcaption></figure>

3. 삭제할 정책을 선택한 후 목록 상단 **\[정책 삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.47.05.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.47.15.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 정책 목록에서 삭제된 것을 확인할 수 있습니다.

### 방화벽 연결 형상 조회

메뉴에서 Security > 방화벽 메뉴를 클릭 후 정책을 조회할 방화벽의 **\[방화벽 연결]** 버튼을 클릭합니다. 연결 형상 탭을 클릭하여 정책 목록을 조회합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-02-07 오후 5.50.56.png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. 방화벽이 비정상 상태로 나와요.**
>
> A. 방화벽 상태가 **비정상** 인 경우 시스템 관리자(sddc.ktcloud@kt.com)에게 문의하시기 바랍니다.
