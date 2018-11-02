---
title: A.23   ordered 지시문 예제
ms.date: 11/04/2016
ms.assetid: f8fa761b-7fc5-4447-95f9-8571e9ca31bf
ms.openlocfilehash: 2868b771fd57613981f3c6458b48493a1b26eee4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50472282"
---
# <a name="a23---examples-of-the-ordered-directive"></a>A.23   ordered 지시문 예제

사용 하 여 순서가 지정 된 섹션이 여러 개 있을 수 있기를 `for` 으로 지정 된 된 `ordered` 절. 첫 번째 예제에서는 비규격 이므로 API는 다음을 지정 합니다.

"사용 하는 루프의 반복을 `for` 구문을 실행 해서는 안 동일 `ordered` 지시문 보다 하며 한 번 실행 하면 안 둘 이상의 `ordered` 지시문입니다." (참조 [2.6.6 섹션](../../parallel/openmp/2-6-6-ordered-construct.md) 22 페이지)

호환 되지 않는이 예제에서는 모든 반복 순서가 지정 된 섹션 2를 실행합니다.

```
#pragma omp for ordered
for (i=0; i<n; i++)
{
    ...
    #pragma omp ordered
    { ... }
    ...
    #pragma omp ordered
    { ... }
    ...
}
```

에서는 다음 준수 예제는 `for` 개를 사용 하 여 순서가 지정 된 섹션:

```
#pragma omp for ordered
for (i=0; i<n; i++)
{
    ...
    if (i <= 10)
    {
        ...
        #pragma omp ordered
        { ... }
    }
    ...
    (i > 10)
    {
        ...
        #pragma omp ordered
        { ... }
    }
    ...
}
```