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

# Volume Type 관리(수정)

***

## 개요

Volume TYpe

플랫폼에서 제공하는 Volume 상품과 OpenStack Volume Type과 연결을 관리합니다.

### 구성

<table><thead><tr><th width="178.24700239808152">분류</th><th>설명</th></tr></thead><tbody><tr><td>Volume Product</td><td>SDDC Platform 사용자들에게 제공하는 Volume 상품을 의미합니다.</td></tr><tr><td>Volume Type</td><td>OpenStack에서 실제 Volume이 생성될 때 사용되는 Volume 구분을 의미합니다.</td></tr></tbody></table>

### OpenStack의 Volume Type(<mark style="color:red;">상용기준 재작성 필요</mark>)

<table><thead><tr><th width="166.12538651196826">이름</th><th width="128">종류</th><th>설명</th></tr></thead><tbody><tr><td>_<em>DEFAULT_</em></td><td></td><td>기본 설정된 Volume Type과 맵핑되어 있다. 현재 NETAPP으로 설정되어있음</td></tr><tr><td></td><td>NetApp</td><td></td></tr><tr><td></td><td>PowerFlex</td><td></td></tr></tbody></table>

## 사용 가이드

### Volume Product 목록 조회

사용자에게 제공하는 Volume Product 목록을 조회합니다.

1. 시스템 관리 > OpenStack 관리 > Volume 관리 메뉴를 클릭합니다.
2. 화면 왼쪽 Volume Product 목록 정보를 확인합니다.
   * 사용: 사용자들에게 Volume Type 제공 여부를 결정합니다.

<figure><img src="../../.gitbook/assets/image (336).png" alt=""><figcaption></figcaption></figure>

### Volume Product 생성

사용자에게 제공할 Volume Product를 생성합니다.

{% hint style="info" %}
**참고**

* 사용 여부를 사용으로 설정해야 사용자에게 Volume Product가 노출됩니다.
{% endhint %}

1. 시스템 관리 > OpenStack 관리 > Volume 관리 메뉴를 클릭합니다.
2. 화면 왼쪽 Volume Product 목록 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (337).png" alt=""><figcaption></figcaption></figure>

3. Volume Product 생성 팝업 창에서 정보를 입력한 후 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (338).png" alt=""><figcaption></figcaption></figure>

### Volume Product 수정

Volume Product 사용 여부와 이름 수정 기능을 제공합니다.

{% hint style="danger" %}
**주의**

* Volume Type이 연결되지 않은 Volume Product는 반드시 미사용 상태로 변경해야 하며, 그렇지 않을 경우 Volume 생성 시 오류가 발생할 수 있습니다.
{% endhint %}

1. 시스템 관리 > OpenStack 관리 > Volume 관리 메뉴를 클릭합니다.
2. 화면 왼쪽 Volume Product 목록 상단에 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (313).png" alt=""><figcaption></figcaption></figure>

3. Volume Product 수정 팝업 창에서 정보를 입력한 후 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (318).png" alt=""><figcaption></figcaption></figure>

### Volume Product 삭제

사용하지 않는 Volume Product를 삭제합니다.

{% hint style="danger" %}
**주의**

* Volume Type을 삭제할 경우, 기존 생성된 Volume에서 상품 정보가 노출되지 않습니다.
* Volume Type을 삭제할 경우 연결된 OpenStack Volume Type의 연결이 해제됩니다.
{% endhint %}

1. 시스템 관리 > OpenStack 관리 > Volume 관리 메뉴를 클릭합니다.
2. 삭제할 Volume Product를 선택하고 목록 상단에 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (314).png" alt=""><figcaption></figcaption></figure>

3. 삭제 팝업 창에서 삭제할 대상을 확인 후 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (319).png" alt="" width="375"><figcaption></figcaption></figure>

### Volume Type 관리하기

#### Volume Type 연결하기

사용자에게 노출할 Volume Product를 실제 OpenStack Volume Type과 연결합니다.

{% hint style="danger" %}
**주의**

* OpenStack Volume Type은 하나의 Volume Product만 연결할 수 있다.
* 연결된 Volume Type을 사용하려면 반드시 설정 메뉴에서 대상 여부를 체크해야 합니다.
{% endhint %}

1. 시스템 관리 > OpenStack 관리 > Volume 관리 메뉴를 클릭합니다.
2. Volume Type을 연결할 Volume Product를 선택합니다.
3. 화면 오른쪽 Volume Type 목록 상단에 **\[동기화]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (317).png" alt=""><figcaption></figcaption></figure>

4. 화면 왼쪽 Volume Product 목록 상단에 **\[연결]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (315).png" alt=""><figcaption></figcaption></figure>

5. Volume Type 연결 팝업 창에서 원하는 Volume Type을 선택 후 **\[연결]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (320).png" alt=""><figcaption></figcaption></figure>

6. 연결한 Volume Type을 선택 후 상단에 **\[설정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (321).png" alt=""><figcaption></figcaption></figure>

7. 설정 팝업 창에서 대상 여부를 선택 후 **\[설정]** 버튼을 클릭합니다.
   * 대상 여부: Volume Type에 대한 사용 여부 체크

<figure><img src="../../.gitbook/assets/image (323).png" alt="" width="375"><figcaption></figcaption></figure>

#### Volume Type 연결 해제하기

Volume Product에 연결된 OpenStack Volume Type을 해제합니다. Volume Type 연결을 해제하더라도 기존에 생성된 Volume은 영향 받지 않습니다.

1. 시스템 관리 > OpenStack 관리 > Volume 관리 메뉴를 클릭합니다.
2. Volume Type을 연결할 Volume Product를 선택한다.
3. Volume Type 목록 상단에 **\[해제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (316).png" alt=""><figcaption></figcaption></figure>

4. Volume Type 해제팝업 창에서 원하는 Volume Type을 선택 후 **\[해제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (339).png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. Volume Product에 여러 개의 Volume Type이 연결되어있을 경우, Volume 생성 시 어떤 Type으로 생성되나요?**
>
> **A.** 연결 목록에서 첫 번째 Volume Type으로 Volume이 생성됩니다. 따라서 원하는 Volume Type으로 생성될 수 있도록 목록에서 사용하지 않는 Volume Type은 관리 대상에서 제외해야 합니다.

> **Q. 동일한 Volume Type이 A -> B Volume Product로 연결 정보가 변경될 경우, 해당 Volume Type을 사용하는 Volume의 Product Type은 어떻게 되나요?**
>
> **A.** 변경된 Volume Product 정보로 제공됩니다.
