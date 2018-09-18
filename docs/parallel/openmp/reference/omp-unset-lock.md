---
title: omp_unset_lock | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- omp_unset_lock
dev_langs:
- C++
helpviewer_keywords:
- omp_unset_lock OpenMP function
ms.assetid: 68fcb728-040b-4bad-979e-aaecb9097a4e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 6b0b7b796ce5db6cfe23eea3608db171ff38e263
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46059067"
---
# <a name="ompunsetlock"></a>omp_unset_lock
잠금을 해제합니다.  
  
## <a name="syntax"></a>구문  
  
```  
void omp_unset_lock(  
   omp_lock_t *lock  
);  
```  
  
### <a name="parameters"></a>매개 변수
  
*lock*<br/>
형식 변수의 [omp_lock_t](../../../parallel/openmp/reference/omp-lock-t.md) 사용 하 여 초기화 된 [omp_init_lock](../../../parallel/openmp/reference/omp-init-lock.md), 스레드에 의해 소유 및 함수에서 실행 합니다.  
  
## <a name="remarks"></a>설명  
 자세한 내용은 [3.2.4 omp_unset_lock and omp_unset_nest_lock 함수](../../../parallel/openmp/3-2-4-omp-unset-lock-and-omp-unset-nest-lock-functions.md)합니다.  
  
## <a name="example"></a>예제  
 참조 [omp_init_lock](../../../parallel/openmp/reference/omp-init-lock.md) 사용 하는 예제에 대 한 `omp_unset_lock`합니다.  
  
## <a name="see-also"></a>참고 항목  
 [함수](../../../parallel/openmp/reference/openmp-functions.md)