---
title: A.12   atomic 지시문 사용
ms.date: 11/04/2016
ms.assetid: d3ba3c87-413d-4efa-8a45-8a7f28ab0164
ms.openlocfilehash: 0f75b182e2cae11f0e72d5ca1e67f887294e8f69
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50504444"
---
# <a name="a12---using-the-atomic-directive"></a>A.12   atomic 지시문 사용

다음 예제에서는 경합 상태를 방지 (요소의 동시 업데이트 *x* 여러 스레드에 의해)를 사용 하 여 합니다 `atomic` 지시문 ([2.6.4 섹션](../../parallel/openmp/2-6-4-atomic-construct.md) 19 페이지):

```
#pragma omp parallel for shared(x, y, index, n)
    for (i=0; i<n; i++)
    {
        #pragma omp atomic
            x[index[i]] += work1(i);
        y[i] += work2(i);
    }
```

사용 하는 이점은 `atomic` 지시문이이 예제에서 두 개의 다른 요소의 병렬로 발생할 수 x 업데이트 수 있다는 점입니다. 경우는 `critical` 지시문 ([2.6.2 섹션](../../parallel/openmp/2-6-2-critical-construct.md) 18 페이지에서) 다음의 요소를 업데이트 하는 모든 대신 사용한 *x* 순차적으로 (하지만 아닌 순서를 보장) 실행 하는 합니다.

`atomic` 지시문은 C 또는 c + + 문을 바로 다음에 적용 됩니다.  결과적으로 요소의 *y* 이 예제에서 자동으로 업데이트 되지 않습니다.