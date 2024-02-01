# Nas Routing 관리(이미지)

***

## 개요

Nas Routing 은 Nas Shared Storage를 사용하기 위한 네트워크 연결 기능입니다. Nas Shared Storage가 생성 되면, 해당 Tenant에 Nas Routing은 자동으로 생성됩니다.  사용자 Subnet이 추가되면 자동으로 Nas Routing에 연결됩니다. Nas Routing이 생성되지 않거나, 연결 설정이 되지 않은 Subnet 에서는 Nas Shared Storage 를 사용할 수 없습니다.

Nas Routing 관리를 통해,  Nas Shared Storage를 사용하기 위한 네트워크 설정을 확인 할 수 있습니다.

## 사용 가이드

### Nas Routing 목록 조회

SDDC 플랫폼 통해 생성된 모든 Nas Routing 을 조회하는 기능입니다.

메뉴 시스템 관리 > 리소스 관리 > Nas Routing 관리에서 Nas Routing 목록을 조회합니다.

이미지

### Nas Routing 연결 관리

Nas Routing에 연결된 Subnet 목록을 관리 하는 기능입니다. 연결되지 않은 Subnet을 추가 할 수 있습니다.

1. Nas Routing을 선택하여 **\[Routing Table 관리]** 버튼을 클릭합니다.

이미지

2. 추가할 Subnet이 있으면, 선택하여 추가합니다.

이미지

3. Routing Table 목록에서 연결된 Subnet을 확인합니다.
