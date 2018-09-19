---
title: OMP_NUM_THREADS | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- OMP_NUM_THREADS
dev_langs:
- C++
helpviewer_keywords:
- OMP_NUM_THREADS OpenMP environment variable
ms.assetid: 4b558124-1387-4c30-a6a5-ff5345a9ced6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 39f45b9c81d5339b2b6afe4c77fdc9bac6b5d731
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46091168"
---
# <a name="ompnumthreads"></a>OMP_NUM_THREADS
의해 재정의 되지 않는 병렬 지역의 스레드의 최대 수를 설정 [omp_set_num_threads](../../../parallel/openmp/reference/omp-set-num-threads.md) 하거나 [num_threads](../../../parallel/openmp/reference/num-threads.md)합니다.  
  
## <a name="syntax"></a>구문  
  
```  
set OMP_NUM_THREADS[=num]  
```  
  
### <a name="parameters"></a>매개 변수
  
*num*<br/>
Visual c + + 구현에서 64 최대 병렬 지역의 하려는 스레드의 최대 수입니다.  
  
## <a name="remarks"></a>설명  
 합니다 **OMP_NUM_THREADS** 환경 변수 재정의 될 수 있습니다 합니다 [omp_set_num_threads](../../../parallel/openmp/reference/omp-set-num-threads.md) 함수 또는 [num_threads](../../../parallel/openmp/reference/num-threads.md)합니다.  
  
 기본값은 `num` Visual c + +에서의 OpenMP 표준 구현은 하이퍼 스레딩을 Cpu를 포함 하 여 가상 프로세서의 수입니다.  
  
 자세한 내용은 [4.2 OMP_NUM_THREADS](../../../parallel/openmp/4-2-omp-num-threads.md)합니다.  
  
## <a name="example"></a>예제  
 다음 명령 집합을 **OMP_NUM_THREADS** 환경 변수를 16:  
  
```  
set OMP_NUM_THREADS=16  
```  
  
 다음 명령은의 현재 설정을 표시 합니다 **OMP_NUM_THREADS** 환경 변수:  
  
```  
set OMP_NUM_THREADS  
```  
  
## <a name="see-also"></a>참고 항목  
 [환경 변수](../../../parallel/openmp/reference/openmp-environment-variables.md)