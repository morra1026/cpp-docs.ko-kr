---
title: 2.2 조건부 컴파일
ms.date: 11/04/2016
ms.assetid: 8f9c914d-736c-48cf-899d-c8029dbe1e32
ms.openlocfilehash: 9dc107ee9e5328df205d4b6f826f71c23abfb3ba
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50658551"
---
# <a name="22-conditional-compilation"></a>2.2 조건부 컴파일

_**OPENMP** 10 진 상수와 매크로 이름이 OpenMP 규격 구현에서 정의 된 *yyyymm*, 연도 및 월의 승인 된 사양을 수 있습니다. 이 매크로는의 주체를 사용 해야 합니다.는 **#define** 또는 **#undef** 전처리 지시문입니다.

```
#ifdef _OPENMP
iam = omp_get_thread_num() + index;
#endif
```

공급 업체 확장 openmp를 정의 하는 경우 추가 미리 정의 된 매크로 지정할 수 있습니다.