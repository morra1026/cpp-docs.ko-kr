---
title: num_threads | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- num_threads
dev_langs:
- C++
helpviewer_keywords:
- num_threads OpenMP clause
ms.assetid: 09a56fc8-25c7-43e4-bbb5-71cb955d0b93
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: d3485d534cf279863b241abcd26195cdde7fea19
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46016288"
---
# <a name="numthreads"></a>num_threads
스레드 팀에서 스레드 수를 설정합니다.  
  
## <a name="syntax"></a>구문  
  
```  
num_threads(num)  
```  
  
### <a name="parameters"></a>매개 변수
  
*num*<br/>
스레드 수  
  
## <a name="remarks"></a>설명  
 합니다 `num_threads` 절에 동일한 기능을 합니다 [omp_set_num_threads](../../../parallel/openmp/reference/omp-set-num-threads.md) 함수입니다.  
  
 `num_threads` 다음 지시문에 적용 됩니다.  
  
-   [parallel](../../../parallel/openmp/reference/parallel.md)  
  
-   [for](../../../parallel/openmp/reference/for-openmp.md)  
  
-   [섹션](../../../parallel/openmp/reference/sections-openmp.md)  
  
 자세한 내용은 [2.3 parallel 구문](../../../parallel/openmp/2-3-parallel-construct.md)합니다.  
  
## <a name="example"></a>예제  
 참조 [병렬](../../../parallel/openmp/reference/parallel.md) 사용 하는 예제에 대 한 `num_threads` 절.  
  
## <a name="see-also"></a>참고 항목  
 [절](../../../parallel/openmp/reference/openmp-clauses.md)