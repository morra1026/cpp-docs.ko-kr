---
title: omp_set_dynamic | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- omp_set_dynamic
dev_langs:
- C++
helpviewer_keywords:
- omp_set_dynamic OpenMP function
ms.assetid: 3845faf2-a0ca-45a5-ae70-2a7a6164f1e8
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 6032503f0b9ccb7d3492f1337165c9db7ec2113a
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46373911"
---
# <a name="ompsetdynamic"></a>omp_set_dynamic

런타임에서 후속 병렬 영역에서 사용할 수 있는 스레드 수를 조정할 수 있는지를 나타냅니다.

## <a name="syntax"></a>구문

```
void omp_set_dynamic(
   int val
);
```

### <a name="parameters"></a>매개 변수

*val*<br/>
런타임에서 후속 병렬 영역에서 사용할 수 있는 스레드 수를 조정할 수 있으면 여부를 나타내는 값입니다.  0이 아니면 0 이면 런타임에서 스레드 수를 조정할 수, 런타임에서 스레드 수를 동적으로 조정 되지 않습니다.

## <a name="remarks"></a>설명

스레드 수는 설정한 값을 초과할 수 없습니다 [omp_set_num_threads](../../../parallel/openmp/reference/omp-set-num-threads.md) 하거나 [OMP_NUM_THREADS](../../../parallel/openmp/reference/omp-num-threads.md)합니다.

사용 하 여 [omp_get_dynamic](../../../parallel/openmp/reference/omp-get-dynamic.md) 의 현재 설정을 표시 하려면 `omp_set_dynamic`합니다.

에 대 한 설정을 `omp_set_dynamic` 의 설정을 재정의 합니다 [OMP_DYNAMIC](../../../parallel/openmp/reference/omp-dynamic.md) 환경 변수입니다.

자세한 내용은 [3.1.7 omp_set_dynamic 함수](../../../parallel/openmp/3-1-7-omp-set-dynamic-function.md)합니다.

## <a name="example"></a>예제

```
// omp_set_dynamic.cpp
// compile with: /openmp
#include <stdio.h>
#include <omp.h>

int main()
{
    omp_set_dynamic(9);
    omp_set_num_threads(4);
    printf_s("%d\n", omp_get_dynamic( ));
    #pragma omp parallel
        #pragma omp master
        {
            printf_s("%d\n", omp_get_dynamic( ));
        }
}
```

```Output
1
1
```

## <a name="see-also"></a>참고 항목

[함수](../../../parallel/openmp/reference/openmp-functions.md)