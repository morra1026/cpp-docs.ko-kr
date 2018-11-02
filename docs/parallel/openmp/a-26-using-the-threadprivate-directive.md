---
title: A.26   threadprivate 지시문 사용
ms.date: 11/04/2016
ms.assetid: 6eda76c2-c4f1-4208-a900-e0ea98a53eca
ms.openlocfilehash: 8ea810f8fbf8076b28464faafb72f5797d4a1a66
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50465431"
---
# <a name="a26---using-the-threadprivate-directive"></a>A.26   threadprivate 지시문 사용

다음 예제에 사용 하는 방법을 보여 줍니다 합니다 `threadprivate` 지시문 ([2.7.1 섹션](../../parallel/openmp/2-7-1-threadprivate-directive.md) 23 페이지) 각 스레드에 별도 카운터를 제공 합니다.

**예제 1:**

```
int counter = 0;
#pragma omp threadprivate(counter)

int sub()
{
    counter++;
    return(counter);
}
```

**예제 2:**

```
int sub()
{
    static int counter = 0;
    #pragma omp threadprivate(counter)
    counter++;
    return(counter);
}
```