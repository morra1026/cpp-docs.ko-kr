---
title: 중요 한 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- Critical
dev_langs:
- C++
helpviewer_keywords:
- critical OpenMP directive
ms.assetid: 2ab87d6d-5ca4-43ae-9f0a-1f517a6a2bab
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c93382886587520e09e2a4035964d33b529b38c7
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46412576"
---
# <a name="critical"></a>Critical

한 번에 하나의 스레드에서 코드는만 실행 됩니다 지정 합니다.

## <a name="syntax"></a>구문

```
#pragma omp critical [(name)]
{
   code_block
}
```

## <a name="arguments"></a>인수

*name*<br/>
(선택 사항) 중요 한 코드를 식별 하는 이름입니다. Note는 이름을 괄호로 묶어야 합니다.

## <a name="remarks"></a>설명

합니다 **중요 한** 지시문 없는 OpenMP 절을 지원 합니다.

자세한 내용은 [중요 한 2.6.2 생성](../../../parallel/openmp/2-6-2-critical-construct.md)합니다.

## <a name="example"></a>예제

```
// omp_critical.cpp
// compile with: /openmp
#include <omp.h>
#include <stdio.h>
#include <stdlib.h>

#define SIZE 10

int main()
{
    int i;
    int max;
    int a[SIZE];

    for (i = 0; i < SIZE; i++)
    {
        a[i] = rand();
        printf_s("%d\n", a[i]);
    }

    max = a[0];
    #pragma omp parallel for num_threads(4)
        for (i = 1; i < SIZE; i++)
        {
            if (a[i] > max)
            {
                #pragma omp critical
                {
                    // compare a[i] and max again because max
                    // could have been changed by another thread after
                    // the comparison outside the critical section
                    if (a[i] > max)
                        max = a[i];
                }
            }
        }

    printf_s("max = %d\n", max);
}
```

```Output
41
18467
6334
26500
19169
15724
11478
29358
26962
24464
max = 29358
```

## <a name="see-also"></a>참고 항목

[지시문](../../../parallel/openmp/reference/openmp-directives.md)