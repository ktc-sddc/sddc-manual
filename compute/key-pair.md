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

# Key Pair

***

## 개요

Key Pair는 SSH Private/Public Key Pair를 생성하여 Server 연결 시 자격 증명 입증에 사용하는 서비스입니다.

{% hint style="danger" %}
**주의**

* 생성된 Private Key는 생성 직후 1회만 다운로드 가능하며 분실 시 복구가 불가능하므로 다운로드 받은 후 안전한 곳에 주의하여 관리하시기 바랍니다.
{% endhint %}

## 사용 가이드

### **Key Pair 목록 조회**

1. Compute > Key Pair 메뉴를 클릭합니다.
2. Key Pair 목록 정보를 확인합니다.

<figure><img src="../.gitbook/assets/image (605).png" alt=""><figcaption></figcaption></figure>

### **Key Pair 생성**

1. Compute > Key Pair 메뉴를 클릭합니다.
2. 목록 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (388).png" alt=""><figcaption></figcaption></figure>

3. 생성 팝업 창에서 정보를 입력하고 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (389).png" alt="" width="375"><figcaption></figcaption></figure>

4. 생성이 완료되면 Private Key가 브라우저에서 자동으로 다운로드 됩니다.

<figure><img src="../.gitbook/assets/image (391).png" alt=""><figcaption></figcaption></figure>

### **Key Pair 삭제**

{% hint style="danger" %}
**주의**

* 삭제된 Key Pair는 복구가 불가능하기 때문에 삭제 대상이 맞는지 반드시 확인 바랍니다.
{% endhint %}

1. Compute > Key Pair 메뉴를 클릭합니다.
2. Key Pair 목록에서 삭제할 대상을 선택하고 상단에 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (392).png" alt=""><figcaption></figcaption></figure>

3. 삭제 팝업 창에서 대상을 확인하고 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (393).png" alt="" width="375"><figcaption></figcaption></figure>

## FAQ

> **Q. Key Pair 비밀번호를 잃어버리면 어떻게 하나요?**
>
> **A.** Key Pair 비밀번호 복구는 불가능합니다. 시스템 관리자(sddc.ktcloud@kt.com)에게 문의바랍니다.

> **Q. Key Pair를 삭제할 경우 기존 Server는 어떻게 되나요?**
>
> **A.** Key Pair는 새로운 Server를 생성하는 순간에 Public Key가 적용됩니다. 콘솔에서 Key Pair를 삭제하더라도 이미 적용하여 사용 중인 Server에서는 기존의 Private Key로 연결이 가능합니다.

> **Q. Server의 Key Pair를 변경할 수 있나요?**
>
> **A.** Server 생성 시 적용한 Key Pair는 수정이 불가능합니다. 변경을 원하시면 시스템 관리자(sddc.ktcloud@kt.com)에게 문의바랍니다.
