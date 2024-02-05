# Load Balancer 관리

***

## 개요

Load Balancer 생성, 수정, 삭제, Listener 관리 등을 제공하는 기능입니다.

등록된 멤버 서버로 수신 트래픽을 분산시켜 서버의 가용성을 높이고 시스템 가동률을 조절하는 역할을 수행합니다. 이를 통해 예기치 못한 서버의 장애 또는 예정된 변경 작업 등에 대하여 중단 없이 대응할 수 있도록 지원합니다.

#### Load Balancer 유형

Load Balancer는 사용 가능한 프로토콜에 따라 Network, Application 두 가지 타입으로 구분됩니다.

<table><thead><tr><th width="152">유형</th><th width="538">설명</th></tr></thead><tbody><tr><td><strong>NETWORK</strong></td><td>L4 Lyaer에서 동작하는 Load Balancer이며, TCP 프로토콜을 지원합니다.</td></tr><tr><td><strong>APPLICATION</strong><br><strong>(출시 예정)</strong></td><td>L7 Lyaer에서 동작하는 Load Balancer이며, HTTP, HTTPS 프로토콜을 지원합니다.</td></tr></tbody></table>

## 사용 가이드

### Load Balancer 목록 조회

Tenant 내에서 사용 중인 Load Balancer 목록을 조회합니다.

1. Network > Load Balancer > Load Balancer 관리 메뉴를 클릭합니다.
2. Load Balancer 목록 정보를 확인합니다.

* Load Balancer 상태

Load Balancer는 운영 상태, 배포 상태라는 두 가지 상태를 지니고 있습니다. 운영 상태는 현재 Load Balancer의 상태를 나타내고, 배포 상태는 Load Balancer 동작 제어에 따른 완료 상태를 의미합니다.

**운영 상태**

<table data-full-width="false"><thead><tr><th width="159">상태(영문)</th><th width="165.72950819672133">상태(한글)</th><th>설명</th></tr></thead><tbody><tr><td><strong>ONLINE</strong></td><td>온라인</td><td>사용 가능한 상태입니다.</td></tr><tr><td><strong>DRAINING</strong></td><td>신규 연결 차단</td><td>멤버 객체에서만 사용되며, 일시적으로 멤버의 기존 연결은 유지한 채 신규 연결은 차단됩니다.</td></tr><tr><td><strong>OFFLINE</strong></td><td>오프라인</td><td>모든 연결을 차단합니다.</td></tr><tr><td><strong>DEGRADED</strong></td><td>비정상</td><td>하위 객체가 Error 상태일 경우 발생합니다.</td></tr><tr><td><strong>ERROR</strong></td><td>장애</td><td>사용 불가능한 상태입니다.</td></tr><tr><td><strong>UNMANAGED</strong></td><td>비정상</td><td>관리되지 않은 상태이며, 관리자에게 문의가 필요합니다.</td></tr></tbody></table>

**배포 상태**

<table data-full-width="false"><thead><tr><th width="173">상태(영문)</th><th width="165.72950819672133">상태(한글)</th><th>설명</th></tr></thead><tbody><tr><td><strong>ACTIVE</strong></td><td>온라인</td><td>사용 가능한 상태입니다.</td></tr><tr><td><strong>DELETED</strong></td><td>신규 연결 차단</td><td>이미 삭제된 상태입니다.</td></tr><tr><td><strong>ERROR</strong></td><td>장애</td><td>배포 과정에서 실패한 상태입니다.</td></tr><tr><td><strong>IN_PROGRESS</strong></td><td>진행 중</td><td>배포가 진행 중인 상태입니다.</td></tr><tr><td><strong>UNMANAGED</strong></td><td>비정상</td><td>관리되지 않은 상태이며, 관리자에게 문의가 필요합니다.</td></tr></tbody></table>

### Load Balancer 상세 보기

Load Balancer 목록 화면에서 특정 Load Balancer를 선택하면 상세 정보를 확인할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (655).png" alt=""><figcaption></figcaption></figure>

&#x20;이 때 하위 메뉴 탭에서 **\[Listener 정보]**를 클릭하면 Load Balancer에서 사용 중인 Listener 목록을 확인할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (656).png" alt=""><figcaption></figcaption></figure>

### Load Balancer 생성

Tenant에서 사용할 Load Balancer를 생성할 수 있습니다.

{% hint style="info" %}
**참고**

* Load Balancer 생성을 위해서는 할당될 Subnet 내 3개 이상의 Network Interface가 필요합니다.
* Load Balancer 사용을  위해서는 출발지와 Loadbalancer가 속한 서브넷과의  네트워크 설정이 선행되어야 합니다.
* Listener의 경우 하나의 Load Balancer에서 동일한 Port 사용은 불가능합니다.
{% endhint %}

1. Network > Load Balancer > Load Balancer 메뉴로 이동합니다.
2. 목록 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (646).png" alt=""><figcaption></figcaption></figure>

3. Load Balancer, Listener 생성 정보를 순차적으로  입력한 후  **\[생성]** 버튼을 클릭합니다.

* Load Balancer 정보 입력

<figure><img src="../../.gitbook/assets/image (647).png" alt=""><figcaption></figcaption></figure>

* Listener 정보 입력

하나의 Load Balancer에서는 동일한 Port는 사용할 수 없으며, Load Balancer 타입에 따라 사용 가능한 프로토콜이 결정됩니다.

<figure><img src="../../.gitbook/assets/image (648).png" alt=""><figcaption></figcaption></figure>



### Load Balancer 수정

생성된 Load Balancer 정보를 수정하는 기능입니다.

1. Network > Load Balancer > Load Balancer 메뉴로 이동합니다.
2. 목록 상단에 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (649).png" alt=""><figcaption></figcaption></figure>

3. 수정 정보를 입력하고, **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (652).png" alt="" width="343"><figcaption></figcaption></figure>

### Load Balancer 삭제

필요 없는 Load Balancer를 삭제하는 기능입니다.

{% hint style="info" %}
**참고**

* Load Balancer 삭제 시 하위 Listener도 함께 삭제됩니다.
* Load Balacner에 할당된 Network Interface는 자동으로 반환됩니다.
* Load Balancer에 연결된 Member Group이 존재할 경우 삭제가 불가합니다.
{% endhint %}

1. Network > Load Balancer > Load Balancer 메뉴로 이동합니다.
2. 목록 상단에 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (650).png" alt=""><figcaption></figcaption></figure>

3. 삭제 대상을 확인하고 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (653).png" alt="" width="345"><figcaption></figcaption></figure>

### Listener 관리

#### Listener 목록 조회

1. Network > Load Balancer > Load Balancer 메뉴로 이동합니다.
2. 대상 Load Balancer를 선택 후 목록 상단에 **\[Listener 관리]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (651).png" alt=""><figcaption></figcaption></figure>

3. 선택한 Load Balancer에서 사용 중인 Listener 목록을 확인합니다.

<figure><img src="../../.gitbook/assets/image (654).png" alt=""><figcaption></figcaption></figure>

#### Listener 생성

1. Network > Load Balancer > Load Balancer > Listener 관리메뉴로 이동합니다.
2. 목록 상단에 추가할 Listener 정보를 입력하고 **\[+ 추가]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (657).png" alt=""><figcaption></figcaption></figure>

#### Listener 수정

{% hint style="info" %}
참고

* Listener의 경우 Protocol 및 Port 수정은 불가능합니다.
* 최대 연결 세션수는 10 \~ 60,000까지 입력 가능합니다.
{% endhint %}

1. Network > Load Balancer > Load Balancer > Listener 관리메뉴로 이동합니다.
2. 수정할 Listner를 입력하고 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (658).png" alt=""><figcaption></figcaption></figure>

3. 수정 정보를 입력하고 \[수정] 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (660).png" alt="" width="338"><figcaption></figcaption></figure>

#### Listener 삭제

{% hint style="info" %}
참고

* Listener에 연결된 Member Group이 존재할 경우 삭제가 불가능합니다.
* Load Balancer 삭제 시 연결된 Listener도 함께 삭제됩니다.
{% endhint %}

1. Network > Load Balancer > Load Balancer > Listener 관리메뉴로 이동합니다.
2. 삭제할 Listener를 선택하고 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (662).png" alt=""><figcaption></figcaption></figure>

3. 삭제 대상을 확인하고 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (661).png" alt="" width="339"><figcaption></figcaption></figure>

## FAQ

>
