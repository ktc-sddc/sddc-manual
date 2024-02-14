# Share Type 관리(new)

## 개요

Share Type은 Openstack 에서 Share 스토리지 볼륨을 생성할 때 어떤 백엔드 스토리지 또는 드라이버와 연결할지 결정합니다. 예를 들어 SSD, HDD로 백엔드가 다르게 구성된 스토리지 시스템이 있다면 각각에 대한 Share Type을 생성하여 사용자가 원하는 백엔드 스토리지를 선택할 수 있도록 제공합니다.

Share Type 관리 기능에서는 Openstack에서 정의한 Share Type 정보를 동기화하는 기능을 제공합니다. SDDC Platform 관리자는 해당 정보를 활용하여 Share Storage 상품을 정의하고 관리합니다.



### OpenStack의 Share Type(<mark style="color:red;">상용기준 재작성 필요</mark>)

<table><thead><tr><th width="216.12538651196826">이름</th><th width="90">종류</th><th>설명</th></tr></thead><tbody><tr><td>NetApp-Share-Thin</td><td>NetApp</td><td></td></tr><tr><td>NetApp-Share-Thick</td><td>NetApp</td><td></td></tr></tbody></table>



## 사용가이드

### Share Type 동기화

Openstack의 Share Type 정보를 SDDC 플랫폼으로 동기화하는 기능입니다.

1. 시스템 관리 > Openstack 관리 > Share Type 관리 메뉴를 클릭합니다.
2. Share Type 목록 정보를 확인합니다.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="149">속성</th><th>설명</th></tr></thead><tbody><tr><td>상품</td><td>해당 Share Type으로 정의된 상품 정보를 표기합니다.</td></tr><tr><td>이름</td><td>Openstack에서 정의한 Share Type 이름입니다.</td></tr><tr><td>관리대상</td><td>사용자 노출 여부를 결정합니다. 해지된 Share Type의 경우 상품 등록이 불가능합니다.</td></tr></tbody></table>

3. 목록 상단에 **\[동기화]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

4. Openstack에 추가 또는 제거된 Share Type 정보가 동기화 되었는지 확인합니다.



### Share Type 설정

{% hint style="info" %}
**참고**

* 최초 동기화된 Share Type의 관리대상 정보 기본값은 **"해지"** 상태입니다. 상품으로 사용하기 위해서는 설정이 필요합니다.
* 기존에 상품으로 등록된 Share Type은 해지가 불가능합니다.
* Share Type은 중복으로 상품 등록이 불가능합니다.
{% endhint %}

1. 관리대상 설정할 Share Type을 선택한 후 상단에 **\[설정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

2.  관리대상 여부를 확인 후 **\[설정]** 또는 **\[해지]** 버튼을 클릭합니다.

    <figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. Share Volume 상품에 여러 개의 Share Type이 연결되어있을 경우, Share Volume 생성 시 어떤 Type으로 생성되나요?**
>
> **A.** 연결 목록에서 첫 번째 Share Type으로 Share Volume이 생성됩니다. 따라서 원하는 Share Type으로 생성될 수 있도록 목록에서 사용하지 않는 Share Type은 관리 대상에서 제외해야 합니다.

> **Q. 동일한 Share Type이 A -> B 상품으로 연결 정보가 변경될 경우, 해당 Share Type을 사용하는 Share Volume의 상품 정보는 어떻게 되나요?**
>
> **A.** 변경된 상품 정보로 제공됩니다.

> **Q. 상품으로 사용 중인 Share Type이 Openstack에서 제거될 경우 어떻게 되나요?**
>
> **A.** 상품 정보 표기에 오류가 생길 수 있습니다. Openstack에서 Share Type을 삭제하기 전에 반드시 기존에 사용 중인 리소스가 있는지 확인해야합니다.
