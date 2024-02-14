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

# Access History

***

## 개요

REST API를 사용하여 SDDC Platform 내 서비스를 사용한 이력 정보를 보여줍니다. SDDC 플랫폼 내에서 발생한 모든 사용자의 활동 이력과 리소스 변경 이력 정보를 확인할 수 있습니다.&#x20;



## 사용 가이드

### Access History 목록 조회

메뉴에서 시스템 관리 > 이력 관리 > Access History 를 클릭하여 Access History 목록을 조회합니다

<figure><img src="../../.gitbook/assets/image (644).png" alt=""><figcaption></figcaption></figure>





### Access History 검색 조회

검색 조건을 통해 Access History 를 조회하는 기능입니다.

<figure><img src="../../.gitbook/assets/image (643).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="189.30456852791878">속성</th><th>설명</th></tr></thead><tbody><tr><td>성공 여부</td><td>HTTP 요청에 대한 성공/실패 여부입니다.</td></tr><tr><td>요청 유형</td><td>HTTP Method 유형을 의미합니다. (POST / PATCH / PUT / DELETE)</td></tr><tr><td>요청 URL</td><td>요청의 URL 을 의미합니다.</td></tr><tr><td>접근 IP</td><td>플랫폼 내 작업을 수행한 접속자의 접근 IP를 의미합니다.</td></tr><tr><td>접속자</td><td>접속자 이름입니다.</td></tr><tr><td>조회 시작일</td><td>Access History 생성일에 대한 조회 시작일을 의미합니다.</td></tr><tr><td>조회 종료일</td><td>Access History 생성일에 대한 조회 종료일을 의미합니다.</td></tr><tr><td>초기화</td><td>입력한 검색 조건을 초기화합니다.</td></tr></tbody></table>





### 상세 보기 기능

Access History 목록 중 행을 클릭하여 화면 하단부에서 상세 이력을 확인 할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (645).png" alt=""><figcaption></figcaption></figure>



