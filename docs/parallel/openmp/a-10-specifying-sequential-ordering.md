---
title: A.10   순차적 정렬 지정
ms.date: 11/04/2016
ms.assetid: 5c65a9b1-0fc5-4cad-a5a9-9ce10b25d25c
ms.openlocfilehash: 4e3a146e1bca988f46cf7a7ee504644f96dab67e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50575255"
---
# <a name="a10---specifying-sequential-ordering"></a>A.10   순차적 정렬 지정

정렬 섹션 ([2.6.6 섹션](../../parallel/openmp/2-6-6-ordered-construct.md) 22 페이지) 순차적으로 병렬로 수행 되는 작업의 출력을 정렬 하는 데 유용 합니다. 다음 프로그램 순차적에서 인덱스를 출력 합니다.

```
#pragma omp for ordered schedule(dynamic)
    for (i=lb; i<ub; i+=st)
        work(i);
void work(int k)
{
    #pragma omp ordered
        printf_s(" %d", k);
}
```