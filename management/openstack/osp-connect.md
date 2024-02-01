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

# OpenStack 환경 설정

***

## 개요

SDDC Platform과 OpenStack 간의 연동을 위한 설정정보를 관리하는 기능입니다.



## 사용 가이드

### OpenStack 환경설정 추가

OpenStack 연결을 위한 환경설정 정보에 대해 Json 포맷으로 추가할 수 있는 기능을 제공합니다.

{% hint style="info" %}
**참고**

* 가져오기 기능을 통해 기존에 작성된 Json 파일을 추가할 수 있습니다.
* 환경설정 정보 추가/수정 시 설정한 정보가 즉시 반영되지 않고, 반드시 애플리케이션(Container)을 재실행 해야 합니다.
{% endhint %}

1. 시스템 관리 > OpenStack 관리 > OpenStack 환경 설정 메뉴를 클릭합니다.
2. 왼쪽 상단에 **\[OSP 추가]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (340).png" alt=""><figcaption></figcaption></figure>

3. OpenStack 환경 설정 정보를 Json 포맷으로 입력 후 **\[변환]** 또는 **\[맞춤]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (343).png" alt=""><figcaption></figcaption></figure>

4. 입력한 설정 정보가 맞는지 검증 후 **\[추가]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (344).png" alt=""><figcaption></figcaption></figure>

### OpenStack 환경설정 수정

OpenStack 연결 관련 환경 설정 정보에 대해 수정할 수 있습니다.

{% hint style="info" %}
**참고**

* 기존에 작성했던 환경 설정 정보를 내보내기 기능을 통해 백업해둘 수 있습니다.
* 환경설정 정보 추가/수정 시 설정한 정보가 즉시 반영되지 않고, 반드시 애플리케이션(Container)을 재실행 해야 합니다.
{% endhint %}

1. 시스템 관리 > OpenStack 관리 > OpenStack 환경 설정 메뉴를 클릭합니다.
2. 왼쪽 상단에 **\[OSP 수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (345).png" alt=""><figcaption></figcaption></figure>

3. OpenStack 환경 설정 정보 수정 후 **\[변환]** 또는 **\[맞춤]** 버튼을 클릭합니다.
4. 입력한 설정 정보가 맞는지 검증 후 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (348).png" alt=""><figcaption></figcaption></figure>

### 초기 Security Group 설정하기

OpenStack 환경설정에서 설정한 admin Project의 default Security Group을 설정합니다.

{% hint style="info" %}
**참고**

* 초기 설정 이후에는 Security Group에 대한 추가적인 작업을 진행하지 않습니다.
{% endhint %}

1. 시스템 관리 > OpenStack 관리 > OpenStack 환경 설정 메뉴를 클릭합니다.
2. **\[초기 S/G 설정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (346).png" alt=""><figcaption></figcaption></figure>

3. 팝업 창의 **\[설정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (347).png" alt="" width="375"><figcaption></figcaption></figure>
