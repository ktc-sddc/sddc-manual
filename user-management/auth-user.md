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

# 사용자 관리

***

## 개요

플랫폼에 접근 가능한 일반 사용자와 ROLE이 부여된 LDAP 사용자를 관리합니다.

### 목록 조회

1. 사용자 관리 > 사용자 관리 메뉴를 클릭합니다.
2. 사용자 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (324).png" alt=""><figcaption></figcaption></figure>



### 플랫폼 일반 사용자 등록

플랫폼 일반 사용자를 등록합니다. 일반 사용자는 사용자 ROLE이 자동으로 부여됩니다.

1. 사용자 관리 > 사용자 관리 메뉴를 클릭합니다.
2. 목록 상단에 **\[등록]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (325).png" alt=""><figcaption></figcaption></figure>

3. 등록 팝업 창에서 정보를 입력합니다.
   * 아이디 : 아이디를 입력합니다.
   * 이름 : 이름을 입력합니다.
   * 비밀번호 : 최소 8자리 이상 문자, 숫자, 특수문자를 조합하여 입력합니다.
     * 허용된 특수문자 : \~!@#$%^&\*\_-+=\`|(){}\[]:;"'<>,.?/
   * 비밀번호(확인) : 앞서 입력한 비밀번호를 다시 한번 입력합니다.
   * 이메일 : 이메일 규칙에 맞게 작성합니다.
   * 전화번호 : 핸드폰 번호를 입력합니다.
4. 팝업 창 우측 하단의 **\[등록]** 버튼을 클릭합니다.
5. 팝업 창이 닫히고, 등록한 사용자를 사용자 관리 화면에서 확인 할 수 있습니다.

<figure><img src="../.gitbook/assets/image (525).png" alt=""><figcaption></figcaption></figure>

### 사용자 정보 수정

플랫폼 일반 사용자 정보를 수정합니다. LDAP 연동 사용자는 수정이 불가능합니다.

1. 사용자 관리 > 사용자 관리 메뉴를 클릭합니다.
2. 수정 할 사용자를 선택 후 목록 상단에 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (332).png" alt=""><figcaption></figcaption></figure>

3. 수정 팝업 창에서 정보를 입력 및 선택합니다.
   * 이메일 : 이메일 규칙에 맞게 작성합니다.
   * 전화번호 : 핸드폰 번호를 입력합니다.
   * 계정상태 : 활성/비활성에 따라 플랫폼 접근이 허용/제한됩니다.
4. 팝업 창 우측 하단의 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (328).png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, 수정한 사용자 정보를 사용자 관리 화면에서 확인할 수 있습니다.

### 비밀번호 초기화

플랫폼 일반 사용자의 비밀번호를 초기화합니다. LDAP 연동 사용자는 비밀번호 초기화가 불가능합니다.

{% hint style="danger" %}
**주의**

* 사용자에게 비밀번호 초기화 요청을 받은 경우, 증적 자료를 남긴 후 비밀번호 초기화를 진행 해주시기를 바랍니다.
* 비밀번호 초기화 이후, 사용자는 초기화 여부를 알 수 없기 때문에 별도로 안내해주시기를 바랍니다.
* 비밀번호가 초기화된 사용자는 반드시 개인정보 수정 기능을 통해 새 비밀번호로 변경해야 합니다.
{% endhint %}

1. 사용자 관리 > 사용자 관리 메뉴를 클릭합니다.
2. 비밀번호 초기화 할 일반 사용자를 선택 후 목록 상단에 **\[비밀번호 초기화]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (333).png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[초기화]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (329).png" alt="" width="375"><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, 해당 사용자의 비밀번호는 아이디로 초기화 됩니다.

### 사용자 삭제

플랫폼 일반 사용자의 계정을 삭제합니다. LDAP 연동 사용자는 삭제가 불가능합니다.

1. 사용자 관리 > 사용자 관리 메뉴를 클릭합니다.
2. 삭제 할 사용자를 선택 후 목록 상단에 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (334).png" alt=""><figcaption></figcaption></figure>

3. 팝업 창 우측 하단의 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (330).png" alt="" width="375"><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, 삭제된 사용자 정보는 사용자 관리 화면에서 보이지 않게 됩니다.

### ROLE 회수

플랫폼 일반 사용자와 LDAP 연동 사용자의 ROLE을 회수합니다. ROLE이 회수된 사용자는 플랫폼 접근이 제한됩니다.

{% hint style="info" %}
**참고**

ROLE이 회수 된 사용자는 미승인 사용자 관리 화면에서 ROLE을 부여할 수 있습니다.
{% endhint %}

1. 사용자 관리 > 사용자 관리 메뉴를 클릭합니다.
2. ROLE을 회수 할 사용자를 선택 후 **\[ROLE 회수]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (335).png" alt=""><figcaption></figcaption></figure>

3. 선택한 사용자의 아이디, 이름 및 적용된 ROLE 유형을 확인할 수 있습니다.
4.  팝업 창 우측 하단의 **\[회수]** 버튼을 클릭합니다.\


    <figure><img src="../.gitbook/assets/image (527).png" alt=""><figcaption></figcaption></figure>
5. 팝업 창이 닫히고, ROLE이 회수 된 사용자 정보는 사용자 관리 화면에서 보이지 않습니다.

## FAQ

> **Q. 시스템 관리자 계정은 어떻게 등록하나요?**
>
> **A.** 시스템 관리자 계정의 경우, 시스템 관리자(sddc.ktcloud@kt.com)에게 요청하시기를 바랍니다.

> **Q. 관리자 계정은 어떻게 등록하나요?**
>
> **A.** 관리자 계정의 경우, 먼저 사용자 관리 메뉴에서 등록 된 사용자의 ROLE을 회수 후 미승인 사용자 관리 메뉴에서 관리자 ROLE을 부여할 수 있습니다.

> **Q. 비밀번호를 변경하는 기능이 보이지 않습니다.**
>
> **A.** 사용자 관리 메뉴에서 시스템 관리자와 관리자는 비밀번호 초기화만 가능하고, 비밀번호 변경은 불가능합니다. 비밀번호 변경은 로그인한 User의 개인정보 수정 기능을 통해 개별적으로 수행할 수 있습니다.
>
> * 로그인 > 상단 오른쪽 사용자 아이콘 클릭 > 계정관리 클릭 > 개인정보 수정 - 비밀번호 변경 버튼 클릭
