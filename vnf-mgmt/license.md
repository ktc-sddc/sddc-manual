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

# License

***

## 개요

NFV Instance를 네트워크에 연결하고, VNF 기능을 사용하기 위해 인증 정보를 담고 있는 License를 관리할 수 있습니다. License는 여러 Spec을 지원하도록 설정이 가능합니다.

> **주의**
>
> * HA 설정이 적용된 VNF Package라면, VNF Package의 Spec을 만족하는 License가 두 개 이상 존재해야 합니다.
> * 사용 중인 License는 다른 NFV Instance에서 사용할 수 없습니다.

## 사용 가이드

### License 목록 조회

왼쪽 메뉴에서 VNF 관리 > 기준 정보 > License를 클릭하여 License 목록을 조회합니다.

<figure><img src="../.gitbook/assets/image (205).png" alt=""><figcaption></figcaption></figure>

### License 업로드

1. 왼쪽 메뉴에서 VNF 관리 > 기준 정보 > License를 클릭하여 License 목록을 조회합니다.
2. 상단의 업로드 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (206).png" alt=""><figcaption></figcaption></figure>

3. 팝업 창이 나타나면, License 업로드에 필요한 정보를 입력합니다.
   * License 이름 : License의 이름을 입력합니다.
   * 상품 유형 : License의 상품 유형을 선택합니다.
   * License 파일 : 업로드하는 License 파일을 선택합니다.
   * 지원 Spec 목록 : 업로드하려는 License 가 지원하는 Spec을 선택하여 테이블에 추가합니다.
   * 설명 : License에 대한 설명을 입력할 수 있습니다.
4. 팝업창 우측 하단의 업로드 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, License 목록 화면에서 업로드된 License를 확인합니다.

### License 수정

1. 왼쪽 메뉴에서 VNF 관리 > 기준 정보 > License를 클릭하여 License 목록을 조회합니다.
2. License 목록에서 수정하고자 하는 License를 선택 후, 상단의 수정 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (207).png" alt=""><figcaption></figcaption></figure>

3. License 수정 팝업 창이 나타나면, License 정보를 수정합니다.
4.  팝업 창 우측 하단의 수정 버튼을 클릭합니다.

    <figure><img src="../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>
5. 팝업 창이 닫히고, License 목록에서 수정사항이 반영된 것을 확인합니다.

### License 삭제

1. 왼쪽 메뉴에서 VNF 관리 > 기준 정보 > License를 클릭하여 License 목록을 조회합니다.
2. License 목록에서 삭제하고자 하는 License를 선택 후, 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (208).png" alt=""><figcaption></figcaption></figure>

3. License 삭제를 위한 팝업 창이 나타나면, 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (123).png" alt="" width="375"><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, License 목록에서 License가 삭제되었는지 확인합니다.

## FAQ

> **Q. License 삭제가 되지 않습니다.**
>
> A. 해당 License를 사용하여 활성화 된 NFV Instance가 존재할 수 있습니다. 해당 NFV Instance를 먼저 삭제하시고, 다시 시도해주시기 바랍니다.
