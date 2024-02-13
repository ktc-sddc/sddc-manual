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

# Compute Node 모니터링

## 개요

Compute Node 모니터링 기능을 제공합니다.

제공되는 지표는 vCPU, Memory, Disk 가 있습니다.



## 상태 기준값

| 상태 | 기준            | 비고        |
| -- | ------------- | --------- |
| 정상 | 1 \~ 70 (%)   |           |
| 주의 | 70 \~ 90 (%)  |           |
| 경고 | 90 \~ 100 (%) |           |
| 기타 | 0 (%)         | 전체 용량 = 0 |

## Compute Node 모니터링 조회

<figure><img src="../../.gitbook/assets/image (617) (1).png" alt=""><figcaption></figcaption></figure>

## FAQ

> **Q. Compute Node가 하나도 보이지 않아요.**
>
> **A.** [**OpenStack 환경설정**](broken-reference)**의 CNode 동기화를 참고하세요**
