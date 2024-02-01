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

# 🔐 사용자 관리

***

SDDC 플랫폼에 등록되어 있는 사용자 정보 및 권한을 관리합니다.

* [사용자 관리](auth-user.md): 사용자 등록/수정/삭제, 비밀번호 초기화, ROLE 회수 기능을 제공합니다.
* [미승인 사용자 관리](unauth-user.md): SDDC Platform 사용을 신청한 LDAP 사용자의 권한을 관리합니다.

SDDC Platform에서 관리하는 사용자 유형, ROLE 유형, 계정 상태는 다음과 같으니 참고하시기 바랍니다.

#### 사용자 유형

다음 2가지 유형의 사용자가 존재합니다. 사용자 유형에 따라 기능이 제약됩니다.

<table><thead><tr><th width="139">사용자 유형</th><th width="229">설명</th><th>기능</th></tr></thead><tbody><tr><td>일반 사용자</td><td>플랫폼에서 생성한 일반 사용자</td><td>수정, 비밀번호 초기화, 삭제, ROLE 회수</td></tr><tr><td>LDAP 사용자</td><td>LDAP 연동 사용자</td><td>ROLE 회수</td></tr></tbody></table>

#### ROLE 유형

다음 3가지 유형의 ROLE이 존재합니다.

<table><thead><tr><th width="253">ROLE 유형</th><th>설명</th></tr></thead><tbody><tr><td>시스템 관리자</td><td>플랫폼 시스템 접근, 관리를 할 수 있는 ROLE</td></tr><tr><td>관리자</td><td>플랫폼 관리, 운영을 할 수 있는 ROLE</td></tr><tr><td>사용자</td><td>플랫폼 운영을 위한 최소 ROLE</td></tr></tbody></table>

#### 계정 상태

다음 2가지 상태가 존재합니다.

<table><thead><tr><th width="113">계정 상태</th><th width="159">플랫폼 접근</th><th>설명</th></tr></thead><tbody><tr><td>활성</td><td>가능</td><td><p>정상 접근이 가능한 상태입니다.</p><ul><li>12개월 미접속 시 비활성 처리됩니다.</li></ul><ul><li>비밀번호를 5회이상 틀린 경우 비활성 처리됩니다.<br></li></ul></td></tr><tr><td>비활성</td><td>불가</td><td><p>접근이 불가능한 상태입니다.</p><ul><li>1년간 이용하지 않을 경우 계정이 삭제 됩니다.</li></ul></td></tr></tbody></table>
