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

Access History 는 SDDC Platform 내 기능을 통해 REST API를 사용한 이력입니다.&#x20;

#### 구성

<table><thead><tr><th width="194">속성</th><th>설명</th></tr></thead><tbody><tr><td>성공 여부</td><td>요청의 성공 여부를 의미합니다.</td></tr><tr><td>요청 유형</td><td>요청의 HTTP Method 유형을 의미합니다.</td></tr><tr><td>요청 URL</td><td>요청의 URL 을 의미합니다.</td></tr><tr><td>실패 사유</td><td>요청 실패 사유 정보입니다.</td></tr><tr><td>접근 IP</td><td>접근 IP 를 의미합니다.</td></tr><tr><td>접속자</td><td>접속자 이름입니다.</td></tr><tr><td>접속일시</td><td>접속한 일시 정보입니다.</td></tr><tr><td>요청 값</td><td>요청 시 전달한 정보입니다.</td></tr></tbody></table>

## 사용 가이드

### Access History 목록 조회

전체 Access History 를 조회하는 기능입니다.

왼쪽 메뉴에서 시스템 관리 > 이력 관리 > Access History 를 클릭하여 Access History 목록을 조회합니다

<figure><img src="../../.gitbook/assets/image (299).png" alt=""><figcaption></figcaption></figure>

### Access History 검색 조회

검색 조건을 통해 Access History 를 조회하는 기능입니다.

1. 왼쪽 메뉴에서 시스템 관리 > 이력 관리 > Access History 를 클릭하여 Access History 목록을 조회합니다.
2. 검색 조건을 입력합니다.
   * 성공 여부: 요청의 성공 여부를 의미합니다.
   * 요청 유형: 요청의 HTTP Method 유형을 의미합니다.
   * 요청 URL: 요청 URL 을 의미합니다.
   * 접근 IP : 접근자의 IP 를 의미합니다.
   * 접속자 : 접근한 사용자의 ID 를 의미합니다.
   * 조회 시작일 : Access History 생성일에 대한 조회 시작일을 의미합니다.
   * 조회 종료일 : Access History 생성일에 대한 조회 종료일을 의미합니다.
3. 검색 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (301).png" alt=""><figcaption></figcaption></figure>

### Access History 상세 조회

Access History 를 상세조회하는 기능입니다. 요청 시 전달값 등 보다 상세한 정보를 확인할 수 있습니다.

1. Access History 목록 화면에서 특정 Access History 를 클릭하여 상세보기를 할 수 있습니다.

<figure><img src="../../.gitbook/assets/image (300).png" alt=""><figcaption></figcaption></figure>

## FAQ
