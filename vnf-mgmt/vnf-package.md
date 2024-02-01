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

# VNF Package

***

## 개요

VNF(Virtual Network Functions) 배포를 위한 템플릿에 해당하는 Package 파일을 업로드하고, 삭제하는 기능을 제공합니다. Package 파일 업로드 시, 상품 유형, HA(High Availability) 설정 여부와 Spec을 선택해야 하며 추가적으로 설명을 기입할 수 있습니다.

> **참고**
>
> * VNF Package 파일 수정은 Spec과 설명만 수정 가능합니다.
> * 업로드 한 VNF Package 파일 수정이 필요한 경우, VNF Package를 삭제 후 재 업로드 해야 합니다.

## 사용 가이드

### VNF Package 파일 목록 조회

왼쪽 메뉴에서 VNF 관리 > VNF > VNF Package 를 클릭하여 VNF Package 파일 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (193).png" alt=""><figcaption></figcaption></figure>

### VNF Package 파일 업로드

1. 왼쪽 메뉴에서 VNF 관리 > VNF > VNF Package 를 클릭합니다.
2. 상단의 업로드 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

3. 팝업 창이 나타나면, VNF Package 업로드 정보를 입력합니다
   * 상품 유형 : 업로드 하고자 하는 VNF Package의 상품 유형을 선택합니다.
   * VNF Package 파일 : 업로드하고자하는 VNF Package 파일을 선택합니다.
   * 지원 Spec : VNF Package 파일이 지원하는 Spec을 선택합니다.
   * HA 이중화 : HA 설정 여부를 체크합니다.
   * 설명 : VNF Package 파일에 대한 설명을 입력합니다.
4. 팝업창 우측 하단의 업로드 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

5. VNF Package 목록에서 업로드한 VNF Package를 확인합니다.

### VNF Package 파일 수정

1. 왼쪽 메뉴에서 VNF 관리 > VNF > VNF Package 를 클릭합니다.
2. VNF Package 파일 목록에서 수정하고자 하는 Package 파일을 선택 후, 상단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>

3. 팝업창이 나타나면 VNF Package 수정 정보를 입력합니다. HA 적용 여부와 Spec, 설명을 수정할 수 있습니다.
4. 팝업창 우측 하단 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>

5. VNF Package 목록에서 수정한 VNF Package의 수정 사항을 확인합니다.

### VNF Package 파일 삭제

1. 왼쪽 메뉴에서 VNF 관리 > VNF > VNF Package 를 클릭합니다.
2. VNF Package 파일 목록에서 삭제하고자 하는 Package 파일을 선택 후, 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>

3. 팝업 창이 나타나면, 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (140).png" alt="" width="375"><figcaption></figcaption></figure>

4. VNF Package 목록에서 VNF Package 삭제 여부를 확인합니다.

## FAQ

> **Q. VNF Package 파일 업로드가 되지 않습니다.**
>
> A. 시스템 관리자(sddc.ktcloud@kt.com)에게 문의하시기 바랍니다.

> **Q. VNF Package 파일 삭제가 되지 않습니다.**
>
> A. [VNF Package 삭제](vnf-package.md#vnf-3)를 참고해주시기 바랍니다. 해당 VNF Package 파일을 참조하고 있는 NS Package 파일이 있을 경우, 해당 NS Package 파일을 먼저 삭제하시고 다시 시도해주시기 바랍니다.

> **Q. HA 설정하지 않은 Package 파일도 HA 적용하여 업로드하면 HA 기능을 사용할 수 있나요?**
>
> A. HA 기능을 사용하려면, Package 파일 생성 시 HA 형상에 맞게 생성한 이후 해당 Package 파일을 HA 이중화 적용을 선택하여 파일을 업로드해야 합니다.
