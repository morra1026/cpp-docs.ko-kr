---
title: omp_set_nested | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- omp_set_nested
dev_langs:
- C++
helpviewer_keywords:
- omp_set_nested OpenMP function
ms.assetid: fa1cb08c-7b8b-42c9-8654-2c33dcffb5b6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: fc3506c35dca469febafe21509064abc1726d633
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46116901"
---
# <a name="ompsetnested"></a>omp_set_nested
중첩 된 병렬 처리가 가능 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
void omp_set_nested(  
   int val  
);  
```  
  
### <a name="parameters"></a>매개 변수
  
*val*<br/>
0이 아닌 경우 중첩 된 병렬 처리를 활성화 합니다. 0, 중첩 된 병렬 처리를 해제 합니다.  
  
## <a name="remarks"></a>설명  
 OMP 중첩 사용 하 여 병렬 처리를 켤 수 있습니다 `omp_set_nested`, 하거나 설정 하는 [OMP_NESTED](../../../parallel/openmp/reference/omp-nested.md) 환경 변수입니다.  
  
 에 대 한 설정을 `omp_set_nested` 의 설정 재정의 `OMP_NESTED` 환경 변수입니다.  
  
 사용 하도록 설정 하는 경우 환경 변수 병렬 영역을 중첩 하는 경우 스레드 수가 기하급수적으로 증가 하기 때문에 그렇지 않은 경우 운영 프로그램을 중단 수 있습니다.  예를 들어 4로 설정 하는 OMP 스레드 수가으로 6 번 재귀적 4,096 (6의 4)에 필요 함을 함수 일반적 스레드, 스레드 수가 프로세서 수를 초과 하는 경우 응용 프로그램의 성능이 저하 됩니다. 이 한 가지 예외는 I/O 바인딩 응용 프로그램 것입니다.  
  
 사용 하 여 [omp_get_nested](../../../parallel/openmp/reference/omp-get-nested.md) 의 현재 설정을 표시 하려면 `omp_set_nested`합니다.  
  
 자세한 내용은 [3.1.9 omp_set_nested 함수](../../../parallel/openmp/3-1-9-omp-set-nested-function.md)합니다.  
  
## <a name="example"></a>예제  
  
```  
// omp_set_nested.cpp  
// compile with: /openmp  
#include <stdio.h>  
#include <omp.h>  
  
int main( )   
{  
    omp_set_nested(1);  
    omp_set_num_threads(4);  
    printf_s("%d\n", omp_get_nested( ));  
    #pragma omp parallel  
        #pragma omp master  
        {  
            printf_s("%d\n", omp_get_nested( ));  
        }  
}  
```  
  
```Output  
1  
1  
```  
  
## <a name="see-also"></a>참고 항목  
 [함수](../../../parallel/openmp/reference/openmp-functions.md)