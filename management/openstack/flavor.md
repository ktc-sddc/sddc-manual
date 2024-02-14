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

# Flavor 관리

***

## 개요

컴퓨팅, 메모리와 같이 자주 사용하는 서버 구성 요소 정보를 미리 정의하는 서비스입니다.

서버를 생성할 때, 미리 정의한 Flavor를 이용해 동일한 타입의 서버를 간편하게 구성하여 생성할 수 있습니다. 이 때 사전 정의한 리소스 정보가 적절한 Host와 연결될 수 있도록 OpenStack 관리자를 통한 Host Aggregate 맵핑이 필요합니다.



### 서버 타입 종류

서버 타입은 CPU/RAM으로 구성되어 있으며, 서비스 규모와 목적에 따라 4가지 서버 타입을 제공합니다.

<table><thead><tr><th width="156">서버타입</th><th width="418">특징</th><th>추천 용도</th></tr></thead><tbody><tr><td>Compact</td><td><p>vCPU가 2 core 이하인 저사양 서버입니다.</p><p>운영하는 서비스가 높은 성능을 요구하지 않고, 서버 운영 비용 부담을 덜고자 하는 분들에게 적합합니다.</p></td><td>개발 테스트 서버</td></tr><tr><td>Standard<br>(1:4)</td><td>범용 모델로 다양한 워크 로드에 적합한 서비스를 제공합니다.</td><td>중/대규모 모바일 및 웹 서비스 운영</td></tr><tr><td>High_Memory<br>(1:8)</td><td>대용량 데이터 처리 등과 같은 메모리 집약적 워크 로드에 적합한 서비스를 제공합니다.</td><td>고성능 데이터베이스 서버</td></tr><tr><td>High_CPU<br>(1:2)</td><td>CPU 집약형 모델로<br>많은 연산이 필요한 업무에 최적화된 서버입니다.</td><td>게임 서버</td></tr></tbody></table>



## 관리자 가이드

### Flavor 목록 조회

1. 시스템 관리 > OpenStack 관리 > Flavor 관리 메뉴를 클릭합니다.
2. 플랫폼에서 사용 가능한 Flavor 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/image (747).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="243">속성</th><th>설명</th></tr></thead><tbody><tr><td>카테고리</td><td>CPU, Memory 조합에 따라 정의되는 서버타입 정보입니다.</td></tr><tr><td>상품</td><td>해당 Flavor로 정의된 상품 정보를 표기합니다.</td></tr><tr><td>이름</td><td>OpenStack에서 정의한 Flavor 이름입니다.</td></tr><tr><td>관리대상</td><td>사용자 노출 여부를 결정합니다. 해지된 Flavor의 경우 상품 등록이 불가능합니다.</td></tr></tbody></table>

### Flavor 관리하기

OpenStack과 동기화된 Flavor 목록 중 사용자에게 제공할 Flavor를 제어하는 기능입니다.

{% hint style="info" %}
**참고**

* 관리대상 여부에 따라 사용자 Server 상품 생성 시 해당 Flavor 노출 여부가 결정됩니다.
* 최초 동기화된 Flavor의 경우 관리대상 속성 기본값이 **"해지"** 상태이며, 사용하기 위해서는 설정이 필요합니다.
{% endhint %}

{% hint style="danger" %}
**주의**

* Flavor를 사용하기 위해서는 연결할 Host Aggregate 맵핑 정보가 OpenStack에 제대로 정의되었는지 확인해야 합니다.
{% endhint %}

1. 관리자 기능 > OpenStack 관리 > Flavor 관리 메뉴를 클릭합니다.
2. 변경할 Flavor를 선택 후 상단에 **\[설정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (750).png" alt=""><figcaption></figcaption></figure>

3. Flavor 관리 팝업 창에서 **\[해지]** 또는 **\[설정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (749).png" alt=""><figcaption></figcaption></figure>



### 신규 Flavor 추가하기

SDDC 플랫폼에서 사용할 Flavor를 새로 추가할 수 있습니다. 이를 위해서는 OpenStack 관리자를 통해 신규 Flavor 등록 및 메타 데이터 설정 등이 필요합니다.

{% hint style="danger" %}
**주의**

* 해당 작업은 OpenStack Dashboard -> SDDC Platform순으로 수행합니다.
* 사전 작업으로 OpenStack 내 실제 Flavor가 사전 등록되어 있어야 합니다.
{% endhint %}

1. **\[OpenStack Dashboard]** Flavor 속성값 설정

<table><thead><tr><th width="147.5008872763442">속성명</th><th width="126">값</th><th>설명</th></tr></thead><tbody><tr><td>공용</td><td>True</td><td>Flavor 공유 범위를 의미하며, 모든 테넌트에서 사용하기 위해서는 <strong>"True"</strong>로 설정이 필요합니다.</td></tr></tbody></table>

2. **\[OpenStack Dashboard]** Flavor 메타데이터 설정

<table><thead><tr><th width="226.5008872763442">필드명</th><th width="111">내용</th><th>설명</th></tr></thead><tbody><tr><td>aggregate_instance_extra_specs:<strong>{HA필드명}</strong></td><td>HA 값</td><td>HA와의 연결관계를 설정하는 속성이며, HA 메타데이터 필드명과 값이 제대로 매칭되는지 확인해야합니다.</td></tr></tbody></table>

3. **\[SDDC Platform]** 관리자 기능 > OpenStack 관리 > Flavor 관리 메뉴를 클릭합니다.
4. **\[SDDC Platform]** 상단에 **\[동기화]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (748).png" alt=""><figcaption></figcaption></figure>



## FAQ

> **Q. 사용하고자 하는 Flavor가 없습니다. 서버 타입을 어떻게 추가하나요?**
>
> **A.** 시스템 관리자(sddc.ktcloud@kt.com)에게 문의 하시기 바랍니다.
