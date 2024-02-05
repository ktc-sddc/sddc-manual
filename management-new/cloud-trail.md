# Cloud Trail

## 개요

&#x20;Tenant 내에서 발생한 작업 이력을 수집하여 제공하는 서비스입니다. 서버 생성, 삭제, 서브넷 연결 등 SDDC Platform 내 서비스의 활동 로그를 확인할 수 있습니다.





## 사용 가이드

### Cloud Trail 목록 조회

Tenant 내에서 발생한 Cloud 리소스의 변경 이력을 조회하는 기능입니다.

메뉴에서 Management > Cloud Trail 메뉴를 클릭하여 Cloud Trail 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (608).png" alt=""><figcaption></figcaption></figure>

### Cloud Trail 검색 기능

검색 조건을 설정하여 Cloud Trail를 조회하는 기능입니다.

<figure><img src="../.gitbook/assets/image (609).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="214">조건</th><th>설명</th></tr></thead><tbody><tr><td>Site</td><td>SDDC 플랫폼내 제공하는 Site 단위로 검색합니다.</td></tr><tr><td>서비스 유형</td><td>SDDC 플랫폼에서 제공하는 서비스 단위로 검색합니다. (예시 - Compute, Storage, Network 등)</td></tr><tr><td>상품 명</td><td>서비스 별 제공되는 상품 별로 검색합니다 (예시 - Compute 서비스 유형 하위에서 선택가능한 상품 리스트 - Server, Key Pair, Init Script 등)</td></tr><tr><td>작업자</td><td>사용자를 검색합니다.</td></tr><tr><td>조회시작일 / 조회 종료일</td><td>검색 범주를 지정합니다.</td></tr></tbody></table>



### 상세 보기 기능

<figure><img src="../.gitbook/assets/image (610).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (611).png" alt=""><figcaption></figcaption></figure>

작업상세의 "**상세**"버튼을 클릭하여 작업 세부 내역을 확인합니다.&#x20;

요청과 응답 결과를 표시하여 어떠한 요청을 시도했는지 확인 할 수 있습니다.







## 리소스 정보

Cloud Trail로 확인 가능한 리소스 목록은 아래와 같습니다.

<table><thead><tr><th width="162">서비스 유형</th><th>상품명</th></tr></thead><tbody><tr><td>Compute</td><td>Server</td></tr><tr><td></td><td>Server Snapshot</td></tr><tr><td></td><td>Init Script</td></tr><tr><td></td><td>Key Pair</td></tr><tr><td></td><td>Network Interface</td></tr><tr><td></td><td>Security Group</td></tr><tr><td>Storage</td><td>Block Storage</td></tr><tr><td></td><td>Share Storage</td></tr><tr><td>Network</td><td>Tenant</td></tr><tr><td></td><td>VPC</td></tr><tr><td></td><td>VPC Peering</td></tr><tr><td></td><td>Subnet</td></tr><tr><td></td><td>Subnet Routing</td></tr><tr><td></td><td>Internet Gateway</td></tr><tr><td></td><td>Colocation Gateway</td></tr><tr><td></td><td>Shared Colocation Gateway</td></tr><tr><td></td><td>Load Balancer</td></tr><tr><td>Security</td><td>Firewall</td></tr><tr><td>Management</td><td>Cloud Canvas</td></tr></tbody></table>
