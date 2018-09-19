---
title: 경우 (OpenMP) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- if
dev_langs:
- C++
helpviewer_keywords:
- if OpenMP clause
ms.assetid: db5940b6-2414-4bf8-934d-3edd8393c0f8
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 83e1920ab2cb44815e9547e4f7f4a07999c1c588
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46020955"
---
# <a name="if-openmp"></a>if (OpenMP)
직렬 또는 병렬로 루프를 실행할지 여부를 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
if(expression)  
```  
  
### <a name="parameters"></a>매개 변수
  
*식*<br/>
(0이 아닌)을 true로 평가 하는 경우 발생 하 여 코드가 병렬 지역의 병렬로 실행 하는 정수 식입니다. 식이 false (0)으로 계산 되 면 병렬 영역 (단일 스레드)를 통해 직렬 실행 됩니다.  
  
## <a name="remarks"></a>설명  
 `if` 다음 지시문에 적용 됩니다.  
  
-   [parallel](../../../parallel/openmp/reference/parallel.md)  
  
-   [for](../../../parallel/openmp/reference/for-openmp.md)  
  
-   [섹션](../../../parallel/openmp/reference/sections-openmp.md)  
  
 자세한 내용은 [2.3 parallel 구문](../../../parallel/openmp/2-3-parallel-construct.md)합니다.  
  
## <a name="example"></a>예제  
  
```  
// omp_if.cpp  
// compile with: /openmp  
#include <stdio.h>  
#include <omp.h>  
  
void test(int val)  
{  
    #pragma omp parallel if (val)  
    if (omp_in_parallel())  
    {  
        #pragma omp single  
        printf_s("val = %d, parallelized with %d threads\n",  
                 val, omp_get_num_threads());  
    }  
    else  
    {  
        printf_s("val = %d, serialized\n", val);  
    }  
}  
  
int main( )  
{  
    omp_set_num_threads(2);  
    test(0);  
    test(2);  
}  
```  
  
```Output  
val = 0, serialized  
val = 2, parallelized with 2 threads  
```  
  
## <a name="see-also"></a>참고 항목  
 [절](../../../parallel/openmp/reference/openmp-clauses.md)