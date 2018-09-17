---
title: flush (OpenMP) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- Flush
dev_langs:
- C++
helpviewer_keywords:
- flush OpenMP directive
ms.assetid: 150ca46e-d4f7-4423-b0a4-838df40aeb67
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 5ea89d4feb7a554c2495c11aa8acaeeaa8bc775f
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45722061"
---
# <a name="flush-openmp"></a>flush (OpenMP)
모든 스레드 모든 공유 개체에 대 한 메모리의 동일한 보기를 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
#pragma omp flush [(var)]  
```  
  
## <a name="arguments"></a>인수

*var*<br/>
(선택 사항) 동기화 할 개체를 나타내는 변수의 쉼표로 구분 된 목록입니다. 경우 `var` 지정 하지 않으면 모든 메모리는 플러시됩니다.  
  
## <a name="remarks"></a>설명  
 합니다 **플러시** 지시문 없는 OpenMP 절을 지원 합니다.  
  
 자세한 내용은 [2.6.5 flush 지시문](../../../parallel/openmp/2-6-5-flush-directive.md)합니다.  
  
## <a name="example"></a>예제  
  
```  
// omp_flush.cpp  
// compile with: /openmp   
#include <stdio.h>  
#include <omp.h>  
  
void read(int *data) {  
   printf_s("read data\n");  
   *data = 1;  
}  
  
void process(int *data) {  
   printf_s("process data\n");  
   (*data)++;  
}  
  
int main() {  
   int data;  
   int flag;  
  
   flag = 0;  
  
   #pragma omp parallel sections num_threads(2)  
   {  
      #pragma omp section  
      {  
         printf_s("Thread %d: ", omp_get_thread_num( ));  
         read(&data);  
         #pragma omp flush(data)  
         flag = 1;  
         #pragma omp flush(flag)  
         // Do more work.  
      }  
  
      #pragma omp section   
      {  
         while (!flag) {  
            #pragma omp flush(flag)  
         }  
         #pragma omp flush(data)  
  
         printf_s("Thread %d: ", omp_get_thread_num( ));  
         process(&data);  
         printf_s("data = %d\n", data);  
      }  
   }  
}  
```  
  
```Output  
Thread 0: read data  
Thread 1: process data  
data = 2  
```  
  
## <a name="see-also"></a>참고 항목  
 [지시문](../../../parallel/openmp/reference/openmp-directives.md)