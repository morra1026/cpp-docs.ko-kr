---
title: A.5   critical 지시문 사용
ms.date: 11/04/2016
ms.assetid: 14423018-25b9-4f98-92f2-34c9b0ac0ce0
ms.openlocfilehash: 82497d63acc057fbbcf26f585e42fc8611c08ec4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50545102"
---
# <a name="a5---using-the-critical-directive"></a>A.5   critical 지시문 사용

다음 예제에서는 몇 개의 `critical` 지시문 ([2.6.2 섹션](../../parallel/openmp/2-6-2-critical-construct.md) 18 페이지에서). 이 예제에서는 태스크를 큐에서 제거 되 고 작업 큐 모델을 보여 줍니다. 여러 스레드에서 동일한 작업을 큐에 대 한 보호를 큐 작업 수에 `critical` 섹션입니다. 이 예제에서 두 개의 큐 독립적 이기 때문에 보호 `critical` 서로 다른 이름 가진 지시문 *x 축* 및 *yaxis*합니다.

```
#pragma omp parallel shared(x, y) private(x_next, y_next)
{
    #pragma omp critical ( xaxis )
        x_next = dequeue(x);
    work(x_next);
    #pragma omp critical ( yaxis )
        y_next = dequeue(y);
    work(y_next);
}
```