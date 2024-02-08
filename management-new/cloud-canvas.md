# Cloud Canvas

## 개요

Cloud Canvas는 SDDC 플랫폼 환경 내 인프라 리소스를 안전하고 반복 가능한 방식으로 프로비저닝 할 수 있는 템플릿 기능을 제공합니다.

<table><thead><tr><th width="162">구분</th><th width="612">상세</th></tr></thead><tbody><tr><td><h4 id="id-sddcblueprint-2">서비스 구성요소</h4></td><td><ul><li><strong>리소스</strong><br> - VPC, Subnet, 인스턴스 등 SDDC 플랫폼에서 관리되는 클라우드 서비스 오브젝트<br> - 리소스는 필수 파라미터 정보를 가진 모듈로서 구성</li><li><strong>템플릿</strong> <br> - VPC, Subnet, 인스턴스 등 인프라를 구성하기 위한 리소스모듈과 <br>모듈 간 연관관계 정보가 있는 인프라 구성 형상</li><li><strong>아웃풋</strong><br> - 템플릿에 의해 배포된 리소스의 묶음 단위</li></ul></td></tr><tr><td><strong>대상 리소스</strong></td><td>SDDC 플랫폼에서 제공하는 Cloud Object<br> *SDDC v1.2 기준 Network 리소스 4종 제공 (VPC, Subnet, Route, VPC Peering)</td></tr></tbody></table>







&#x20;&#x20;

## 사용가이드

### 템플릿 생성

SDDC 플랫폼 내 관리자 권한을 가진 사용자는 SDDC 플랫폼 내에서 공통으로 사용할 인프라 형상을 정의한 템플릿을 생성할 수 있습니다.&#x20;

{% hint style="info" %}
본 매뉴얼에서는 Tenant 하위 VPC , Subnet 리소스 생성하는 Case에 대해 설명합니다.
{% endhint %}

1. Management > Cloud Canvas > 템플릿 관리 화면으로 이동합니다.

<figure><img src="../.gitbook/assets/image (670).png" alt=""><figcaption></figcaption></figure>



2. **생성** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (671).png" alt=""><figcaption></figcaption></figure>



1. Step 1. 템플릿 생성을 위한 정보를 입력합니다. \
   \
   1\) 기본 템플릿 구성\
   &#x20;  \- **템플릿 이름**과 **템플릿 설명**을 입력합니다.\
   \
   2\) **다음** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (672).png" alt=""><figcaption></figcaption></figure>

2. Step 2. 템플릿 구성정보를 입력합니다. \


{% hint style="info" %}
리소스 모듈을 추가할때는, 리소스간의 연관관계를 고려하여 순서대로 생성합니다.\
\
예시) \
Case 1. VPC 1개, Subnet 1개\
&#x20;    step 1) VPC 모듈 1개 추가\
&#x20;    step 2) Subnet 모듈 1개 추가\
\
Case 2. VPC 1개, Subnet 2개, Routing 1개\
&#x20;    step 1) VPC 모듈 1개 추가\
&#x20;    step 2) Subnet 모듈 2개 추가 \
&#x20;    step 3) Routing 모듈 1개 추가
{% endhint %}

* Network 리소스 모듈 에서 VPC와 Subnet 모듈을 한번씩 클릭합니다.

<figure><img src="../.gitbook/assets/image (674).png" alt=""><figcaption></figcaption></figure>

* VPC 생성시 필요한 정보를 입력합니다.&#x20;
* Subnet 생성 시 필요한 정보를 입력합니다.\
  &#x20;\- Subnet 생성 시에는 Subnet 이 배포될 VPC 리소스를 선택합니다.

<figure><img src="../.gitbook/assets/image (675).png" alt=""><figcaption></figcaption></figure>

* 우측 Topology 화면에서 리소스가 배포될 형상을 확인할 수 있습니다.
* 배포할 리소스의 정보를 다 입력했다면, "**다음**" 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (676).png" alt=""><figcaption></figcaption></figure>

* 생성할 Object에 대한 정보를 확인한 후 **생성** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (677).png" alt=""><figcaption></figcaption></figure>

* 팝업에서 **생성** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (678).png" alt=""><figcaption></figcaption></figure>



* 템플릿 관리 화면에서 생성한 템플릿 정보를 확인합니다.

<figure><img src="../.gitbook/assets/image (679).png" alt=""><figcaption></figcaption></figure>













### 템플릿 공유

관리자가 생성한 템플릿을 공유하면 테넌트 소유자 권한을 가진 일반 사용자에게 공개됩니다. \
테넌트 소유자 권한을 가진 사용자는 관리자가 공유한 템플릿을 사용하여 템플릿에 정의된 인프라 리소스를 테넌트 내에 프로비저닝 할 수 있습니다.



1. Management > Cloud Canvas > 템플릿 관리 화면으로 이동합니다.
2. 공유할 템플릿을 선택한 후 **공유** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (680).png" alt=""><figcaption></figcaption></figure>

3. 템플릿 공유 여부에 초록색 체크표시가 되었는지 확인합니다.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>





### 템플릿 배포

사용자는 사전에 정의된 템플릿을 사용하여 인프라 리소스를 프로비저닝 할 수 있습니다.

{% hint style="info" %}
템플릿 배포 기능은 테넌트 소유자 (Tenant Owner) 권한을 가진 사용자만 사용할 수 있습니다.
{% endhint %}



1. Management > Cloud Canvas > 템플릿 Repository 화면으로 이동합니다.
2. 사용할 템플릿을 선택한 후 **배포** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (681).png" alt=""><figcaption></figcaption></figure>



3. 템플릿에 정의된 리소스 정보와 형상을 확인 후 **다음** 버튼을 클릭합니다.

{% hint style="info" %}
리소스 이름 및 CIDR 대역 등 리소스 파라미터는 수정할 수 있습니다. 단, 템플릿에 정의된 리소스는 삭제하거나, 연관관계를 수정할 수 없습니다.
{% endhint %}

<figure><img src="../.gitbook/assets/image (682).png" alt=""><figcaption></figcaption></figure>



4. 테넌트에 프로비저닝 할 인프라 리소스 구성 내용을 확인한 후 **배포** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (684).png" alt=""><figcaption></figcaption></figure>

5. 팝업창의 내용을 확인 후 **배포** 버튼을 클릭합니다.

<figure><img src="../.gitbook/assets/image (686).png" alt=""><figcaption></figcaption></figure>





6. Managment > Cloud Canvas > 캔버스 아웃풋 관리 화면으로 이동합니다.
7. 배포 결과를 확인합니다.

<figure><img src="../.gitbook/assets/image (687).png" alt=""><figcaption></figcaption></figure>

8. 각 항목의 **상세** 버튼을 클릭하여 배포한 리소스의 세부 정보를 확인할 수 있습니다.

<figure><img src="../.gitbook/assets/image (688).png" alt=""><figcaption></figcaption></figure>



{% hint style="info" %}
리소스는 템플릿에 정의된 리소스간의 연관관계에 따라 순차적으로 배포되며, 프로세스 중간에 리소스 배포가 실패하는 경우 배포 프로세스는 중단됩니다.&#x20;

이 경우, 프로세스 중 생성에 성공한 리소스는 자동으로 삭제되지 않습니다. 삭제를 희망하는 경우 각 리소스 별 메뉴  (Ex - Network > VPC 메뉴)로 이동하여 Object를 직접 삭제하여야 합니다.
{% endhint %}

{% hint style="info" %}
배포가 실패하는 경우는 다음과 같습니다.\
\
1\)  배포대상 리소스가 Tenant 내 기 생성된 리소스 정보와 중복되는 경우 (리소스 이름 / Cidr 대역 등)

2\) Tenant 내 정의된 리소스 Quota를 초과하여 배포를 시도한 경우
{% endhint %}



