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

# Spec

***

## 개요

가상 CPU(이하 vCPU), Memory 용량, Storage 용량을 포함하는 사양 정보를 관리할 수 있습니다. 해당 정보는 License, VNF Package에서 참조될 수 있습니다.

> **참고**
>
> * 참조되고 있는 Spec은 삭제 및 수정이 불가합니다.
> * 참조되고 있는 Spec을 삭제 또는 수정하기 위해서는 해당 Spec을 참조하고 있는 License 혹은 VNF Package를 수정 또는 삭제해야 합니다.

## 사용 가이드

### Spec 목록 조회

왼쪽 메뉴에서 VNF 관리 > 기준 정보 > Spec을 클릭하여 Spec 목록을 조회합니다.

<figure><img src="../../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure>

### Spec 생성

1. 왼쪽 메뉴에서 VNF 관리 > 기준 정보 > Spec을 클릭하여 Spec 목록을 조회합니다.
2. 상단의 생성 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (210).png" alt=""><figcaption></figcaption></figure>

3. 팝업 창이 나타나면, Spec 생성에 필요한 필수 정보를 입력합니다.
   * Spec 이름 : Spec 이름을 입력합니다.
   * vCPU : vCPU 개수를 입력합니다.
   * Memory : Memory 용량을 입력합니다.
   * Storage : Storage 용량을 입력합니다.
4. 팝업창 우측 하단의 생성 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

5. 팝업 창이 닫히고, Spec 목록 화면에서 생성된 Spec을 확인합니다.

### Spec 수정

1. 왼쪽 메뉴에서 VNF 관리 > 기준 정보 > Spec을 클릭하여 Spec 목록을 조회합니다.
2. Spec 목록에서 수정하고자 하는 Spec을 선택한 다음, 상단의 수정 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (211).png" alt=""><figcaption></figcaption></figure>

3. Spec 수정 팝업 창이 나타나면, Spec 정보를 수정합니다.

<figure><img src="../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

4. 팝업 창 우측 하단의 수정 버튼을 클릭합니다.
5. 팝업 창이 닫히고, Spec 목록 화면에서 수정 사항이 반영된 것을 확인합니다.

### Spec 삭제

1. 왼쪽 메뉴에서 VNF 관리 > 기준 정보 > Spec을 클릭하여 Spec 목록을 조회합니다.
2. Spec 목록에서 수정하고자 하는 Spec을 선택한 다음, 상단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (212).png" alt=""><figcaption></figcaption></figure>

3. Spec 삭제를 위한 팝업 창이 나타나면, 팝업 창 우측 하단의 삭제 버튼을 클릭합니다.

<figure><img src="../../.gitbook/assets/image (124).png" alt="" width="375"><figcaption></figcaption></figure>

4. 팝업 창이 닫히고, Spec 목록 화면에서 Spec이 삭제되었는지 확인합니다.

## FAQ

> **Q. Spec 삭제가 되지 않습니다.**
>
> A. [Spec 삭제](spec.md#spec-3)를 참고해주시기 바랍니다. 해당 Spec을 참조하고 있는 [VNF Package](../vnf-package.md) 파일, [NS Package](../vnf/ns-package.md) 파일, [License](../license.md) 혹은 [NFV Instance](../vnf/nfv-instance.md)가 있을 경우, 해당 항목들을 먼저 삭제하시고 다시 시도해주시기 바랍니다.
