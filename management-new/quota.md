# Quota

## 개요

Quota 는 리소스 생성 한도를 의미하며, 이를 초과하여 리소스를 생성할 수 없습니다. 기본적으로 리소스 별 기본 Quota 가 존재하며, 변경 요청을 통해 리소스에 적용된 Quota 값을 변경할 수 있습니다.

### 용어

<table><thead><tr><th width="183">이름</th><th>설명</th></tr></thead><tbody><tr><td>유형</td><td><ul><li>DEFAULT : 기본 Quota 값이 적용됨을 의미.</li><li>CUSTOMIZED : 변경 요청된 값이 적용됨을 의미.</li></ul></td></tr><tr><td>Resource</td><td>Quota 제한 리소스를 의미.</td></tr><tr><td>Resource Scope</td><td>Quota 제한 범위를 의미.</td></tr><tr><td>기본 Quota</td><td>기본적으로 제공되는 리소스 생성 한도를 의미.</td></tr><tr><td>적용된 Quota</td><td>현재 적용된 리소스 생성 한도를 의미.</td></tr></tbody></table>



## 사용 가이드

### Quota 현황 조회

현재 선택된 Tenant 에 적용된 Quota 정보를 조회하는 기능입니다.

메뉴에서 Management > Quota > Quota 현황 탭을 클릭하여 Quota 현황을 조회합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-31 오후 1.36.25.png" alt=""><figcaption></figcaption></figure>

### Quota 변경 요청 생성

현재 선택된 Tenant 에 적용된 Quota 를 변경 요청하는 기능입니다.

{% hint style="info" %}
**참고**

* Tenant 리소스는 Quota 변경 요청이 불가능합니다.
* 이미 Quota 변경 요청이 진행중인 리소스에 대한 새로운 요청은 생성할 수 없습니다.
{% endhint %}

1. 메뉴에서 Management > Quota > Quota 현황 탭을 클릭하여 Quota 현황을 조회합니다.
2. 변경할 리소스를 선택하고, 목록 상단에서 **\[변경 요청]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-31 오후 1.36.58.png" alt=""><figcaption></figcaption></figure>

3. 변경 요청 팝업 창에서 정보를 입력합니다.
   * 요청 유형 : 목적에 맞는 유형을 선택합니다.
     * 변경 : Quota 를 원하는 값으로 변경.
     * 초기화 : 기본 Quota 가 적용되도록 변경.
   * Quota : 변경 유형의 경우 원하는 Quota 값을 입력합니다.
   * 요청 제목 : 관리자에게 전달하는 요청 제목을 입력합니다.
   * 요청 메시지 : 관리자에게 전달하는 요청 메시지를 입력합니다.
4. 팝업 창 우측 하단의 **\[변경 요청]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-31 오후 1.37.21.png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 생성한 요청을 변경 요청 내역 화면에서 확인 할 수 있습니다.

### Quota 변경 요청 내역 조회

현재 선택된 Tenant 에 대한 Quota 변경 요청 내역을 조회하는 기능입니다.

메뉴에서 Management > Quota > 변경 요청 내역 탭을 클릭하여 변경 요청 내역 목록을 조회합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-31 오후 1.37.52.png" alt=""><figcaption></figcaption></figure>

### Quota 변경 요청 취소

현재 선택된 Tenant 에 대한 Quota 변경 요청 을 취소하는 기능입니다.

{% hint style="info" %}
**참고**

* 요청 상태가 '요청' 인 경우만 취소가 가능합니다.
{% endhint %}

1. 메뉴에서 Management > Quota > 변경 요청 내역 탭을 클릭하여 변경 요청 내역 목록을 조회합니다.
2. 취소할 요청을 선택하고, 목록 상단에서 **\[요청 취소]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-31 오후 1.38.09.png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[변경 취소]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/스크린샷 2024-01-31 오후 1.38.19.png" alt=""><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, 요청 내역 화면에서 삭제된 것을 확인 할 수 있습니다.

## FAQ

> Q. Tenant 의 Quota 를 변경할 수 없을까요?
>
> A. 네, 현재 플랫폼 운영 정책 상 Tenant 는 계정 당 최대 1개로 제한되고 있습니다. 한 계정에서 여러 Tenant 를 관리하고 싶은 경우 [tenant-member.md](../tenant-member.md "mention") 기능을 통해 권한 공유를 해주시기 바랍니다.
