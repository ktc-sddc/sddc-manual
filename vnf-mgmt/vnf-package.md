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

# Network Service Package

***

## 개요

VNF(Virtual Network Functions) 배포를 위한 템플릿에 해당하는 Package 파일을 업로드하고, 삭제하는 기능을 제공합니다. Package 파일 업로드 시, 상품 유형을  입력해야하며, 추가적으로 설명을 기입할 수 있습니다.

> **참고**
>
> * 업로드 한 Network Service Package 파일 수정이 필요한 경우, Network Service Package를 삭제 후 재 업로드 해야 합니다.

## 사용 가이드

### Network Service Package 파일 목록 조회

메뉴에서 VNF 관리 > Network Service Package 를 클릭하여 Network Service Package 파일 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (193).png" alt=""><figcaption></figcaption></figure>

### Network Service Package 파일 업로드

1. 메뉴에서 VNF 관리 > Network Service Package 를 클릭합니다.
2. 상단의 업로드 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

3. VNF 형상 정보를 담고 있는 VNF 데이터 셋 파일을  업로드하여 정보를 확인합니다.
4. Network Service 정보를 담고 있는 NS Package 파일을 업로드하여정보를확인합니다.
5. 업로드하고자 하는 Network Service Package 정보를 확인 후, 생성 버튼을 클릭하여 생성합니다.
6. Network Service Package 목록에서 업로드한 Network Service Package를 확인합니다.

### Network Service Package 파일 삭제

1. 메뉴에서 VNF 관리 > Network Service Package 를 클릭합니다.
2. Network Service Package 파일 목록에서 삭제하고자 하는 Package 파일을 선택 후, 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>

3. 팝업 창이 나타나면, 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (140).png" alt="" width="375"><figcaption></figcaption></figure>

4. Network Service Package 목록에서 Network Service Package 삭제 여부를 확인합니다.

## FAQ

> **Q. Network Service Package 파일 업로드가 되지 않습니다.**
>
> A. 시스템 관리자(sddc.ktcloud@kt.com)에게 문의하시기 바랍니다.

> **Q. Network Service Package 파일 삭제가 되지 않습니다.**
>
> A. 해당 Network Service Package 파일을 참조하고 있는 방화벽이 있을 경우, 해당 Network Service Package 파일을 먼저 삭제하시고 다시 시도해주시기 바랍니다.
