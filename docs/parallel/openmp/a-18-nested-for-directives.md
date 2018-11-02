---
title: A.18   지시문에 중첩됨
ms.date: 11/04/2016
ms.assetid: ae2b2e0b-ec94-43f8-928c-6d621b51f0df
ms.openlocfilehash: dbebcd88489c6fdb00011531e7b74b27ee154b4e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50554295"
---
# <a name="a18---nested-for-directives"></a>A.18   지시문에 중첩됨

다음 예제에서는 `for` 지시문 중첩 ([섹션 2.9](../../parallel/openmp/2-9-directive-nesting.md) 33 페이지) 준수 때문에 내부 및 외부 `for` 병렬 서로 다른 지역에 지시문 바인딩:

```
#pragma omp parallel default(shared)
{
    #pragma omp for
        for (i=0; i<n; i++)
        {
            #pragma omp parallel shared(i, n)
            {
                #pragma omp for
                    for (j=0; j<n; j++)
                        work(i, j);
            }
        }
}
```

앞의 예제는 다음 변형은 규격 이기도합니다.

```
#pragma omp parallel default(shared)
{
    #pragma omp for
        for (i=0; i<n; i++)
            work1(i, n);
}

void work1(int i, int n)
{
    int j;
    #pragma omp parallel default(shared)
    {
        #pragma omp for
            for (j=0; j<n; j++)
                work2(i, j);
    }
    return;
}
```