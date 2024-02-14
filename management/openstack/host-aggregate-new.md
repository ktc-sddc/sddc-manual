# Host Aggregate 관리(new)

## 개요

Host Aggregate(HA)란 Openstack에서 컴퓨팅 호스트(하이퍼바이저)를 논리적인 그룹으로 구분한 것을 말합니다. 이를 통해 컴퓨팅 리소스를 효과적으로 관리할 수 있습니다.&#x20;

예를 들어 GPU 지원이 가능한 호스트를 하나의 HA로 정의할 경우, 인스턴스를 생성할 때 GPU 자원이 필요한 경우 해당 HA를 지정하여 자원을 배치할 수 있습니다.

Host Aggregate 관리 기능에서는 Openstack에서 정의한 Host 그룹 정보를 동기화하는 기능을 제공합니다.

<figure><img src="../../.gitbook/assets/image (734).png" alt=""><figcaption></figcaption></figure>

