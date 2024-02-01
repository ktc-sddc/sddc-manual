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

# NS Package

***

## 개요

NFV(Network Function Virtualization) Instance 생성을 위해 VNF 간 형상 정보를 담은 NS(Network Service) Package 파일을 업로드하고, 삭제하는 기능을 제공합니다. Package 파일 업로드 시, 해당 NS Package가 참조하고 있는 VNF Package와 Instance 생성 시 생성이 필요한 네트워크 인터페이스를 선택해야 하며 추가적으로 설명을 기입할 수 있습니다.

> **참고**
>
> * NS Package 수정 시, 설명만 수정 가능합니다.
> * 참조하고 있는 VNF Package 수정 등의 항목에 대하여 수정이 필요한 경우, 삭제 후 재 업로드 해야 합니다.

## 사용 가이드

### NS Package 파일 조회

왼쪽 메뉴에서 VNF 관리 > VNF > NS Package 를 클릭하여 NS Package 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>

### NS Package 파일 업로드

1. 왼쪽 메뉴에서 VNF 관리 > VNF > NS Package 를 클릭하여 NS Package 파일 목록을 조회합니다.
2. 상단의 업로드 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (190).png" alt=""><figcaption></figcaption></figure>

3. 팝업 창이 나타나면, NS Package 업로드 정보를 입력합니다.
   * NS Package 파일 : 업로드하고자하는 NS Package 파일을 선택합니다.
   * 참조 VNF Package : NS Package 파일이 참조하고 있는 VNF Package 파일을 선택합니다.
   * Interface 정보 : Interface 유형 별 생성 여부를 체크합니다.
   * 설명 : 업로드할 NS Package의 설명을 입력합니다.
4. 팝업창 우측 하단의 업로드 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

5. NS Package 목록에서 업로드한 NS Package를 확인합니다.

### NS Package 파일 수정

1. 왼쪽 메뉴에서 VNF 관리 > VNF > NS Package 를 클릭하여 NS Package 파일 목록을 조회합니다.
2. NS Package 파일 목록에서 수정하고자 하는 Package 파일을 선택 후, 상단의 수정 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure>

3. 팝업 창이 나타나면, NS Package 설명을 수정합니다.
4. 팝업창 우측 하단의 수정 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

5. NS Package 목록에서 수정한 NS Package의 수정 사항을 확인합니다.

### NS Package 파일 삭제

1. 왼쪽 메뉴에서 VNF 관리 > VNF > NS Package 를 클릭하여 NS Package 파일 목록을 조회합니다.
2. NS Package 파일 목록에서 삭제하고자 하는 Package 파일을 선택 후, 좌측 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (192).png" alt=""><figcaption></figcaption></figure>

3. 팝업창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (146).png" alt="" width="375"><figcaption></figcaption></figure>

4. NS Package 목록에서 NS Package 삭제 여부를 확인합니다.

## FAQ

> **Q. NS Package 파일 삭제가 되지 않습니다.**
>
> A. NS Package 삭제(링크)를 참고해주시기 바랍니다. 해당 NS Package 파일을 참조하고 있는 NFV Instance(링크)가 있을 경우, 해당 NFV Instance를 먼저 삭제하시고 다시 시도해주시기 바랍니다.
