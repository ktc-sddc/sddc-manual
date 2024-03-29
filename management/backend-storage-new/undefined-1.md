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

# 환경설정

## 개요

SDDC Platform과 Backend Storage 간의 연동을 위한 설정정보를 관리하는 기능입니다.



## 사용 가이드

### Backend Storage 환경설정 조회

<figure><img src="../../.gitbook/assets/image (730).png" alt=""><figcaption></figcaption></figure>



### Backend Storage 환경설정 생성

OpenStack 연결을 위한 환경설정 정보에 대해 JSON 포맷으로 추가할 수 있는 기능을 제공합니다.

{% hint style="info" %}
**참고**

* 가져오기 기능을 통해 기존에 작성된 JSON 파일을 추가할 수 있습니다.
* 환경설정 정보 추가/수정 시 설정한 정보가 즉시 반영되지 않고, 반드시 애플리케이션(Container)을 재실행 해야 합니다.
{% endhint %}

1. 시스템 관리 > Backend Storage 관리 > 환경 설정 메뉴를 클릭합니다.
2. 왼쪽 상단에 **\[생성]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-13 오전 10.12.39.png" alt=""><figcaption></figcaption></figure>

3. JSON 형식의 데이터를 입력 후, 생성 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (732).png" alt=""><figcaption></figcaption></figure>



### Backend Storage 환경설정 수정

1. 시스템 관리 > Backend Storage 관리 > 환경 설정 메뉴를 클릭합니다.
2. 왼쪽 상단에 **\[수정]** 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/스크린샷 2024-02-13 오전 10.12.39 2.png" alt=""><figcaption></figcaption></figure>

3. JSON 형식의 데이터를 입력 후, 수정 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (733).png" alt=""><figcaption></figcaption></figure>
