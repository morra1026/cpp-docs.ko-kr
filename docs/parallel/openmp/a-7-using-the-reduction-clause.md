---
title: A.7   reduction 절 사용
ms.date: 11/04/2016
ms.assetid: e71e65bc-a25c-4f02-b507-66b52bf950a4
ms.openlocfilehash: ba0b1c9563837314c06949f898938031149d4663
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50618610"
---
# <a name="a7---using-the-reduction-clause"></a>A.7   reduction 절 사용

다음 예제에서는 reduction 절 ([2.7.2.6 섹션](../../parallel/openmp/2-7-2-6-reduction.md) 28 페이지):

```
#pragma omp parallel for private(i) shared(x, y, n) \
                         reduction(+: a, b)
    for (i=0; i<n; i++) {
        a = a + x[i];
        b = b + y[i];
    }
```