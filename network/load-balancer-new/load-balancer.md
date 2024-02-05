# Load Balancer 관리

***

## 개요

Load Balancer 생성, 수정, 삭제, Listener 관리 등을 제공하는 기능입니다.



#### Load Balancer 유형

<table><thead><tr><th width="152">유형</th><th width="538">설명</th></tr></thead><tbody><tr><td><strong>NETWORK</strong></td><td></td></tr><tr><td><strong>APPLICATION</strong></td><td></td></tr></tbody></table>

## 사용 가이드

### Load Balancer 목록 조회

* Load Balancer 상태

Load Balancer는 운영 상태, 배포 상태라는 두 가지 상태를 지니고 있습니다. 운영 상태는 현재 Load Balancer의 상태를 나타내고, 배포 상태는 Load Balancer 동작 제어에 따른 완료 상태를 의미합니.

<table data-full-width="false"><thead><tr><th width="159">상태(영문)</th><th width="165.72950819672133">상태(한글)</th><th>설명</th></tr></thead><tbody><tr><td><strong>ONLI</strong>NE</td><td>온라인</td><td>Server 에 연결이 가능한 상태입니다.</td></tr><tr><td><strong>DRAINING</strong></td><td>신규 연결 차단</td><td>ㅁ\</td></tr><tr><td><strong>DISCONNECT</strong></td><td>신규 연결 차단</td><td>Volume 생성을 실패하였습니다.</td></tr><tr><td><strong>OFFLINE</strong></td><td>오프라인</td><td>Volume 생성 중입니다.</td></tr><tr><td><strong>DEGRADED</strong></td><td>비정상</td><td>Volume을 Server에 연결 중입니다.</td></tr><tr><td><strong>ERROR</strong></td><td>장애</td><td>Server 에서 Volume 연결을 해제하는 중입니다.</td></tr><tr><td><strong>UNMANAGED</strong></td><td>비정상</td><td>관리되지 않은 상태이며, 관리자에게 문의가 필요합니다.</td></tr></tbody></table>

### Load Balancer 생성

### Load Balancer 상세 보기

### Load Balance 수정

### Load Balancer 삭제

### Listener 관리

#### Listener 목록 조회

#### Listener 생성

#### Listener 수정

#### Listener 삭제



## FAQ
