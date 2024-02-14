# Host Aggregate 관리(new)

## 개요

Host Aggregate(HA)란 Openstack에서 컴퓨팅 호스트(하이퍼바이저)를 논리적인 그룹으로 구분한 것을 말합니다. 이를 통해 컴퓨팅 리소스를 효과적으로 관리할 수 있습니다.&#x20;

예를 들어 GPU 지원이 가능한 호스트를 하나의 HA로 정의할 경우, 인스턴스를 생성할 때 GPU 자원이 필요한 경우 해당 HA를 지정하여 자원을 배치할 수 있습니다.

Host Aggregate 관리 기능에서는 Openstack에서 정의한 Host 그룹 정보를 동기화하는 기능을 제공합니다.

&#x20; &#x20;

### OpenStack의 Host Aggregate(<mark style="color:red;">상용기준 재작성 필요</mark>)

<table><thead><tr><th width="158.12538651196826">이름</th><th width="454">Hosts</th><th>설명</th></tr></thead><tbody><tr><td>MD-STG-HDD</td><td><p>1. csnode-ovs-1-8a1803c29-md-staging-sddc.ipc.kt.com</p><p>2. csnode-ovs-2-8a1803c27-md-staging-sddc.ipc.kt.com</p><p>3. csnode-ovs-3-8a1803c31-md-staging-sddc.ipc.kt.com</p></td><td></td></tr><tr><td></td><td></td><td></td></tr></tbody></table>

Adsd

## 사용가이드

### Share Type 동기화

Openstack의 Share Type 정보를 SDDC 플랫폼으로 동기화하는 기능입니다.

1. 시스템 관리 > Openstack 관리 > Share Type 관리 메뉴를 클릭합니다.
2. Share Type 목록 정보를 확인합니다.

<figure><img src="../../.gitbook/assets/image (734).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="149">속성</th><th>설명</th></tr></thead><tbody><tr><td>이름</td><td>Openstack에서 정의한 Host Aggregate 이름입니다.</td></tr><tr><td>Metadata</td><td>Host 그</td></tr><tr><td>Hosts</td><td></td></tr><tr><td>관리대상</td><td></td></tr></tbody></table>

3. 목록 상단에 **\[동기화]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

4. Openstack에 추가 또는 제거된 Share Type 정보가 동기화 되었는지 확인합니다.

