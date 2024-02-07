# Member Group 관리

***

## 개요

Member Group은  Load Balancer의 Listener에 연결되는 Member 집합입니다. 이를 통해 Member에 대한 Monitoring 정책이나 분배 정책 등을 관리합니다.

Member Group 관리 기능에서는 Member Group 생성, 수정, 삭제 및 Health Monitor 관리, Member 관리 등을 제공합니다.



#### 프로토콜 조합

대상 Listener의 프로토콜에 따라 Member Group에서 사용할 수 있는 프로토콜은 아래와 같이 제한됩니다.

**\[프로토콜 조합 표]**

※ Health  Monitor의 경우 Member Group과 무관하게 프로토콜 설정이 가능합니다.



#### Member Group(Member) 상태

Member Group과 Member는 Load Balancer와 마찬가지로 운영 상태, 배포 상태라는 두 가지 상태를 지니고 있습니다. 운영 상태는 현재 Member Group의 상태를 나타내고, 배포 상태는 Member Group 동작 제어에 따른 완료 상태를 의미합니다.

예를 들어 Member Group의 배포 상태가 "**진행 중**"이면서 운영 상태는 "**온라인**"일 수 있으며, 이는 현재 정상 운영 중인 Member Group에 대한 동작 제어(수정, 삭제, Member 추가 등)가 요청되었음을 의미합니다.

* **운영 상태**

<table data-full-width="false"><thead><tr><th width="159">상태(영문)</th><th width="165.72950819672133">상태(한글)</th><th>설명</th></tr></thead><tbody><tr><td><strong>ONLINE</strong></td><td>온라인</td><td>사용 가능한 상태입니다.</td></tr><tr><td><strong>DRAINING</strong></td><td>신규 연결 차단</td><td>멤버 객체에서만 사용되며, 일시적으로 멤버의 기존 연결은 유지한 채 신규 연결은 차단됩니다.</td></tr><tr><td><strong>OFFLINE</strong></td><td>오프라인</td><td>모든 연결을 차단합니다.</td></tr><tr><td><strong>DEGRADED</strong></td><td>비정상</td><td>하위 객체가 Error 상태일 경우 발생합니다.</td></tr><tr><td><strong>ERROR</strong></td><td>장애</td><td>사용 불가능한 상태입니다.</td></tr><tr><td><strong>UNMANAGED</strong></td><td>비정상</td><td>관리되지 않은 상태이며, 관리자에게 문의가 필요합니다.</td></tr></tbody></table>

* **배포 상태**

<table data-full-width="false"><thead><tr><th width="173">상태(영문)</th><th width="165.72950819672133">상태(한글)</th><th>설명</th></tr></thead><tbody><tr><td><strong>ACTIVE</strong></td><td>온라인</td><td>사용 가능한 상태입니다.</td></tr><tr><td><strong>DELETED</strong></td><td>신규 연결 차단</td><td>이미 삭제된 상태입니다.</td></tr><tr><td><strong>ERROR</strong></td><td>장애</td><td>배포 과정에서 실패한 상태입니다.</td></tr><tr><td><strong>IN_PROGRESS</strong></td><td>진행 중</td><td>배포가 진행 중인 상태입니다.</td></tr><tr><td><strong>UNMANAGED</strong></td><td>비정상</td><td>관리되지 않은 상태이며, 관리자에게 문의가 필요합니다.</td></tr></tbody></table>

###

### Member Group 상세 보기

## 사용 가이드

### Member Group 목록 조회

Tenant 내에서 사용 중인 Member Group 목록을 조회합니다.

1. Network > Load Balancer > Member Group 관리 메뉴를 클릭합니다.
2. Member Group 목록 정보를 확인합니다.



Member Group 목록 화면에서 특정 Member Group을 선택하면 상세 정보를 확인할 수 있습니다.

이 때 상단 메뉴 탭에서 **\[Health Monitor 관리]**와 **\[Member 관리]**를 통해서 Member Group의 Health Monitor 정책 및 연결된 Member에 대한 관리 기능을 제공합니다.

### Member Group 생성

Listener에서 사용할 Member Group을 생성할 수 있습니다.

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
