---
title: OMP_SCHEDULE | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- OMP_SCHEDULE
dev_langs:
- C++
helpviewer_keywords:
- OMP_SCHEDULE OpenMP environment variable
ms.assetid: 2295a801-e584-4d2f-826f-7ca4c88846a6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 507067be30db019536ef222a62335244eabfaada
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46413863"
---
# <a name="ompschedule"></a>OMP_SCHEDULE

동작을 수정 합니다 [일정](../../../parallel/openmp/reference/schedule.md) 절 때 `schedule(runtime)` 에 지정 된을 `for` 또는 `parallel for` 지시문입니다.

## <a name="syntax"></a>구문

```
set OMP_SCHEDULE[=type[,size]]
```

## <a name="arguments"></a>인수

*size*<br/>
(선택 사항) 반복의 크기를 지정합니다. `size` 양의 정수 여야 합니다. 기본값은 1, 경우를 제외 하 고 `type` 고정 됩니다. 유효 하지 않은 경우 `type` 는 `runtime`합니다.

*type*<br/>
예약의 종류:

- `dynamic`

- `guided`

- `runtime`

- `static`

## <a name="remarks"></a>설명

OpenMP 표준의 Visual c + + 구현에서 기본값은 `OMP_SCHEDULE=static,0`합니다.

자세한 내용은 [4.1 OMP_SCHEDULE](../../../parallel/openmp/4-1-omp-schedule.md)합니다.

## <a name="example"></a>예제

다음 명령 집합을 **OMP_SCHEDULE** 환경 변수:

```
set OMP_SCHEDULE="guided,2"
```

다음 명령은의 현재 설정을 표시 합니다 **OMP_SCHEDULE** 환경 변수:

```
set OMP_SCHEDULE
```

## <a name="see-also"></a>참고 항목

[환경 변수](../../../parallel/openmp/reference/openmp-environment-variables.md)