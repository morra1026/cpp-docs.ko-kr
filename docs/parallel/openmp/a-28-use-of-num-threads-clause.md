---
title: A.28   num_threads 절 사용
ms.date: 11/04/2016
ms.assetid: 26238da1-902c-49b4-9559-0fbc9eaf7f36
ms.openlocfilehash: 99dd327d0a97f561107ffaa6a6ed1435e3772a41
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50492290"
---
# <a name="a28---use-of-numthreads-clause"></a>A.28   num_threads 절 사용

다음 예제는 `num_threads` 절 ([섹션 2.3](../../parallel/openmp/2-3-parallel-construct.md) 8 페이지). 병렬 영역을 최대 10 개 스레드를 사용 하 여 실행 됩니다.

```
#include <omp.h>
main()
{
    omp_set_dynamic(1);
    ...
    #pragma omp parallel num_threads(10)
    {
        ... parallel region ...
    }
}
```