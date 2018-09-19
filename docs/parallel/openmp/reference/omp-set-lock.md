---
title: omp_set_lock | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- omp_set_lock
dev_langs:
- C++
helpviewer_keywords:
- omp_set_lock OpenMP function
ms.assetid: ded839cb-ca19-403f-8622-eb52ce512d31
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 390090b0f4bf5f8795373db9f61f8365257ee95b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46024914"
---
# <a name="ompsetlock"></a>omp_set_lock
블록 스레드 잠금을 제공 될 때까지 실행 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
void omp_set_lock(  
   omp_lock_t *lock  
);  
```  
  
### <a name="parameters"></a>매개 변수
  
*lock*<br/>
형식 변수의 [omp_lock_t](../../../parallel/openmp/reference/omp-lock-t.md) 사용 하 여 초기화 된 [omp_init_lock](../../../parallel/openmp/reference/omp-init-lock.md)합니다.  
  
## <a name="remarks"></a>설명  
 자세한 내용은 [3.2.3 omp_set_lock and omp_set_nest_lock 함수](../../../parallel/openmp/3-2-3-omp-set-lock-and-omp-set-nest-lock-functions.md)합니다.  
  
## <a name="examples"></a>예제  
 참조 [omp_init_lock](../../../parallel/openmp/reference/omp-init-lock.md) 사용 하는 예제에 대 한 `omp_set_lock`합니다.  
  
## <a name="see-also"></a>참고 항목  
 [함수](../../../parallel/openmp/reference/openmp-functions.md)