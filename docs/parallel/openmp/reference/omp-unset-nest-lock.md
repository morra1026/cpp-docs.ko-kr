---
title: omp_unset_nest_lock | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- omp_unset_nest_lock
dev_langs:
- C++
helpviewer_keywords:
- omp_unset_nest_lock OpenMP function
ms.assetid: 1721d061-3f9c-45d7-b479-a665cd0a121d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 03ea941e793f8c3a9f40e0495442deb71b2ffa93
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46402722"
---
# <a name="ompunsetnestlock"></a>omp_unset_nest_lock

중첩 가능 잠금을 해제합니다.

## <a name="syntax"></a>구문

```
void omp_unset_nest_lock( 
   omp_nest_lock_t *lock 
);
```

### <a name="parameters"></a>매개 변수

*lock*<br/>
형식 변수의 [omp_nest_lock_t](../../../parallel/openmp/reference/omp-nest-lock-t.md) 사용 하 여 초기화 된 [omp_init_nest_lock](../../../parallel/openmp/reference/omp-init-nest-lock.md), 스레드에 의해 소유 및 함수에서 실행 합니다.

## <a name="remarks"></a>설명

자세한 내용은 [3.2.4 omp_unset_lock and omp_unset_nest_lock 함수](../../../parallel/openmp/3-2-4-omp-unset-lock-and-omp-unset-nest-lock-functions.md)합니다.

## <a name="example"></a>예제

참조 [omp_init_nest_lock](../../../parallel/openmp/reference/omp-init-nest-lock.md) 사용 하는 예제에 대 한 `omp_unset_nest_lock`합니다.

## <a name="see-also"></a>참고 항목

[함수](../../../parallel/openmp/reference/openmp-functions.md)