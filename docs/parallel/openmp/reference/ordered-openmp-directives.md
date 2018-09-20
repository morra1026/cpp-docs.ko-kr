---
title: (OpenMP 지시문)를 정렬 합니다. | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- ordered
dev_langs:
- C++
helpviewer_keywords:
- ordered OpenMP directive
ms.assetid: e1aa703e-d07d-4f6a-9b2a-f4f25203d850
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 1d999503a8f5802056c32329bf68e62383cbd53f
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46420857"
---
# <a name="ordered-openmp-directives"></a>ordered (OpenMP 지시문)

해당 코드를 병렬에서 순차 루프와 같은 루프를 실행 해야 지정 합니다.

## <a name="syntax"></a>구문

```
#pragma omp ordered
   structured-block
```

## <a name="remarks"></a>설명

**정렬** 지시문의 동적 범위 내에 있어야 합니다.는 [에 대 한](../../../parallel/openmp/reference/for-openmp.md) 또는 **에 대 한 병렬** 사용 하 여 생성을 **정렬** 절.

합니다 **정렬** 지시문 없는 OpenMP 절을 지원 합니다.

자세한 내용은 [2.6.6 ordered 구문](../../../parallel/openmp/2-6-6-ordered-construct.md)합니다.

## <a name="example"></a>예제

```
// omp_ordered.cpp
// compile with: /openmp
#include <stdio.h>
#include <omp.h>

static float a[1000], b[1000], c[1000];

void test(int first, int last)
{
    #pragma omp for schedule(static) ordered
    for (int i = first; i <= last; ++i) {
        // Do something here.
        if (i % 2)
        {
            #pragma omp ordered
            printf_s("test() iteration %d\n", i);
        }
    }
}

void test2(int iter)
{
    #pragma omp ordered
    printf_s("test2() iteration %d\n", iter);
}

int main( )
{
    int i;
    #pragma omp parallel
    {
        test(1, 8);
        #pragma omp for ordered
        for (i = 0 ; i < 5 ; i++)
            test2(i);
    }
}
```

```Output
test() iteration 1
test() iteration 3
test() iteration 5
test() iteration 7
test2() iteration 0
test2() iteration 1
test2() iteration 2
test2() iteration 3
test2() iteration 4
```

## <a name="see-also"></a>참고 항목

[지시문](../../../parallel/openmp/reference/openmp-directives.md)