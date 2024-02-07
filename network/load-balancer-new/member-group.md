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

## 사용 가이드

### Member Group 목록 조회

Tenant 내에서 사용 중인 Member Group 목록을 조회합니다.

1. Network > Load Balancer > Member Group 관리 메뉴를 클릭합니다.
2. Member Group 목록 정보를 확인합니다.

<figure><img src="../../.gitbook/assets/image (693).png" alt=""><figcaption></figcaption></figure>



### Member Group 상세 보기

Member Group 목록 화면에서 특정 Member Group을 선택하면 상세 정보를 확인할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (694).png" alt=""><figcaption></figcaption></figure>

이 때 상세 정보  메뉴 탭에서 **\[Health Monitor]**와 **\[Member]**를 통해서 Member Group의 Health Monitor 정책 및 연결된 Member에 대한 조회 기능을 제공합니다.

* Health Monitor

<figure><img src="../../.gitbook/assets/image (695).png" alt=""><figcaption></figcaption></figure>

* Member

<figure><img src="../../.gitbook/assets/image (696).png" alt=""><figcaption></figcaption></figure>



### Member Group 생성

Listener에서 사용할 Member Group을 생성할 수 있습니다.

{% hint style="info" %}
**참고**

* Member Group을 생성하기 위해서는 먼저 Load Balancer와 Listener가 필요하다.
* Member Group은 하나의 Listener에서만 사용할 수 있으며, 다른 Member Group에서 사용 중인 Listener는 사용이 불가능하다.
* Health Monitor 정책은 Load Balancer와 Member 간 Health Check 정책을 의미하며, 정책이 정상 동작하기 위해서는 Load Balancer와 Member 간 통신이 선행되어야만 한다.
* Member의 경우 Member Group 내 동일한 IP(Network Interface)에 대해 중복이 불가하다.
{% endhint %}

1. Network > Load Balancer > Member Group 관리 메뉴로 이동합니다.
2. 목록 상단에 **\[생성]** 버튼을 클릭합니다.
3. Member Group, Health Monitor, Member 생성 정보를 순차적으로  입력한 후  **\[생성]** 버튼을 클릭합니다.

1\)  Member Group 생성 정보 입력

<figure><img src="../../.gitbook/assets/image (689).png" alt=""><figcaption></figcaption></figure>

* 분배 정책: Member에 대한 Load Balancer의 분산 알고리즘을 의미하며 3가지 알고리즘을 지원한다.

<table><thead><tr><th width="243">유형</th><th>설명</th></tr></thead><tbody><tr><td>ROUND_ROBIN</td><td>연결된 Member에 대해 순차적으로 분배하는 정책이다.</td></tr><tr><td>SOURCE_IP</td><td>Source IP의 Hash값을 기준으로 분배하는 정책이다.</td></tr><tr><td>LEAST_CONNECTION</td><td>가장 연결이 적은 Member에 대해 우선 분배하는 정책이다.</td></tr></tbody></table>

* 세션 지속성: 사용자  요청이 후 특정 서버로 유지되는 정책을 의미하며, 크게 2가지 타입을 지원하며, 기본 값은 NONE이다.

<table><thead><tr><th width="243">유형</th><th>설명</th></tr></thead><tbody><tr><td>HTTP Cookie 기반<br>(지원 예정)</td><td>사용자의 브라우저에 쿠키를 생성하고 이를 사용하여 특정 서버로의 요청을 유도하는 정책이며, L7 정책(HTTP, HTTPS 프로토콜)에서만 지원합니다.</td></tr><tr><td>SOURCE_IP</td><td>Source IP를 기준으로 동일한 출발지 IP에 대해 기존 서버로 요청을 유도하는 정책이다.</td></tr></tbody></table>



2\) Health Monitor 생성 정보 입력

<figure><img src="../../.gitbook/assets/image (690).png" alt=""><figcaption></figcaption></figure>

* 프로토콜: Load Balancer와 Member 간 연결 체크 시 사용할 네트워크 프로토콜을 정의합니다. 이 때, Member Group의 프로토콜과는 무관하게 설정이 가능하며, PING, TCP, HTTP, HTTPS 4가지를 지원합니다.
* 최대 재시도 횟수: Member와  Load Balancer 간 연결 상태 확인에 실패할 경우 Member의 운영 상태를 "**온라인**" -> "**장애**"로 전환합니다. 이 때, 연결 상태 확인을 위한 최대 연결 체크 시도 횟수를 의미하며, 1 \~ 10까지 지정할 수 있습니다.
* 응답 대기 시간(초):  Member와  Load Balancer 간 연결 상태 확인시 응답 대기 시간을 말하며, 응답 대기 시간은 상태 확인 주기보다 작게 설정되어야 합니다.
* 상태 확인 주기(초):  Member와  Load Balancer 간 연결 체크 주기를 의미합니다.



3\) Member 추가

<figure><img src="../../.gitbook/assets/image (691).png" alt=""><figcaption></figcaption></figure>





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

1. Network > Load Balancer > Load Balancer > Listener 관리 메뉴로 이동합니다.
2. 삭제할 Listener를 선택하고 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (662).png" alt=""><figcaption></figcaption></figure>

3. 삭제 대상을 확인하고 **\[삭제]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (661).png" alt="" width="339"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (692).png" alt=""><figcaption></figcaption></figure>

##

## FAQ

>
