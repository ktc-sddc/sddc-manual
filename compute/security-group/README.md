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

# Security Group

***

## 개요

Security Group은 서버 간 송수신을 제어하여 네트워크 접근 제어 및 관리를 할 수 있는 가상의 방화벽 서비스 입니다. Security Group은 [Security Rule](security-rule.md)들의 집합으로, Security Rule을 통해 서버에서 발생하는 허가 받지 않은 바운드/아웃바운드 트래픽을 제어함으로써 서버를 안전하게 보호할 수 있습니다.

#### Default Security Group

Tenant 생성 시, Default Security Group이 1개 생성되어 제공됩니다.\
Default Security Group은 다음과 같은 Security Rule을 가지며 Rule은 수정, 삭제가 불가능합니다.

* 모든 송신(egress) 허용
* 모든 수신(ingress) 허용

{% hint style="info" %}
**참고**

* Default Security Group은 수정, 삭제가 불가능 합니다.
{% endhint %}

#### 기본 Security Rule

추가적으로 Security Group을 생성할 때에는 다음과 같은 기본 Security Rule이 생성됩니다.\
이때, 제공되는 기본 Security Rule은 Security Group 생성 시에는 수정, 삭제가 불가능하나, 생성이 완료된 이후에는 수정, 삭제가 가능합니다.

* 모든 송신(egress) 허용



## 사용 가이드

### Security Group 목록 조회

1. Compute > Security Group 버튼을 클릭합니다.
2. Security Group 목록을 확인합니다.

<figure><img src="../../.gitbook/assets/image (606).png" alt=""><figcaption></figcaption></figure>

### Security Group 생성

1. Compute > Security Group 버튼을 클릭합니다.
2. 목록 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 1.54.32.png" alt=""><figcaption></figcaption></figure>

1. 생성 팝업 창에서 정보를 입력하고 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 1.56.37.png" alt=""><figcaption></figcaption></figure>

### Security Group 수정

1. Compute > Security Group 버튼을 클릭합니다.
2. 수정할 Security Group을 선택하고 목록 상단에 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 1.54.32 2.png" alt=""><figcaption></figcaption></figure>

1. 수정 팝업 창에서 정보를 입력하고 **\[수정]** 버튼을 클릭합니다. 현재는 이름만 수정 가능합니다.

<figure><img src="../../.gitbook/assets/image (404).png" alt="" width="375"><figcaption></figcaption></figure>

### Security Group 삭제

{% hint style="info" %}
**참고**

* Network Interface에 할당된 Security Group은 삭제가 불가능 합니다.
* Security Rule에서원 Remote(원격)로 사용되는 Security Group은 삭제가 불가능 합니다.
{% endhint %}

1. Compute > Security Group 버튼을 클릭합니다.
2. 삭제할 Security Group을 선택하고 목록 상단에 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 1.54.32 3.png" alt=""><figcaption></figcaption></figure>

1. 삭제 팝업 창에서 대상을 확인하고 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-05 오후 1.57.19.png" alt=""><figcaption></figcaption></figure>

### [Security Rule 관리](security-rule.md)

Security Group의 Rule을 관리하는 기능입니다. 자세한 사항은 링크를 참조하시기 바랍니다.

## FAQ

> **Q. Security Rule은 어떻게 설정해야하나요?**
>
> 자세한 사항은 [Security Rule](security-rule.md)을 참조해 주세요.\
> \
> **Q. Security Group을 서버에 어떻게 적용하나요?**\
> [Network Interface](../network-interface.md)를 참조해 주세요
>
> **Q. Security Group은 최대 몇 개까지 생성 가능한가요?**
>
> Tenant 당개최대 5개까지 생성 할 수 있습니다.
