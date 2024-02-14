# Host Aggregate 관리(new)

## 개요

Host Aggregate(HA)란 OpenStack에서 컴퓨팅 호스트(하이퍼바이저)를 논리적인 그룹으로 구분한 것을 말합니다. 이를 통해 컴퓨팅 리소스를 효과적으로 관리할 수 있습니다.&#x20;

예를 들어 GPU 지원이 가능한 호스트를 하나의 HA로 정의할 경우, 인스턴스를 생성할 때 GPU 자원이 필요한 경우 해당 HA를 지정하여 자원을 배치할 수 있습니다.

Host Aggregate 관리 기능에서는 OpenStack에서 정의한 Host 그룹 정보를 동기화하는 기능을 제공합니다.

### OpenStack의 Host Aggregate(<mark style="color:red;">상용기준 재작성 필요</mark>)

<table><thead><tr><th width="158.12538651196826">이름</th><th width="454">Hosts</th><th>설명</th></tr></thead><tbody><tr><td>MD-STG-HDD</td><td><p>1. csnode-ovs-1-8a1803c29-md-staging-sddc.ipc.kt.com</p><p>2. csnode-ovs-2-8a1803c27-md-staging-sddc.ipc.kt.com</p><p>3. csnode-ovs-3-8a1803c31-md-staging-sddc.ipc.kt.com</p></td><td></td></tr></tbody></table>



## 사용가이드

### Host Aggregate 목록 조회

1. 시스템 관리 > OpenStack 관리 > Image 관리 메뉴를 클릭합니다.
2. 플랫폼에서 사용 가능한 Image 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/image (734).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="149">속성</th><th>설명</th></tr></thead><tbody><tr><td>이름</td><td>OpenStack에서 정의한 Host Aggregate 이름입니다.</td></tr><tr><td>Metadata</td><td>HA와 Flavor를 연결하는 속성이며, Host 그룹 구분의 기준을 의미합니다.</td></tr><tr><td>Hosts</td><td>HA에 속한 Host 리스트입니다.</td></tr></tbody></table>

### Host Aggregate 동기화

OpenStack의 Host Aggregate 정보를 SDDC 플랫폼으로 동기화하는 기능입니다.

1. 시스템 관리 > OpenStack 관리 > Host Aggregate 관리 메뉴를 클릭합니다.
2. Host Aggregate 목록 정보를 확인합니다.
3. 목록 상단에 **\[동기화]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

4. OpenStack에 추가 또는 제거된 Host Aggregate 정보가 동기화 되었는지 확인합니다.



## FAQ

> **Q.**&#x20;
>
> **A.**&#x20;
