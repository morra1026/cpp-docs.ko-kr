---
title: omp_destroy_nest_lock | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- omp_destroy_nest_lock
dev_langs:
- C++
helpviewer_keywords:
- omp_destroy_nest_lock OpenMP function
ms.assetid: 0ab1352b-668f-43dd-b441-31ec4cc53e68
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 1d5cb4e985c82bec859959f374ffe35f33548228
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46377255"
---
# <a name="ompdestroynestlock"></a>omp_destroy_nest_lock

중첩 가능 잠금을 초기화를 취소 합니다.

## <a name="syntax"></a>구문

```
void omp_destroy_nest_lock(
   omp_nest_lock_t *lock
);
```

### <a name="parameters"></a>매개 변수

*lock*<br/>
형식 변수의 [omp_nest_lock_t](../../../parallel/openmp/reference/omp-nest-lock-t.md) 사용 하 여 초기화 된 [omp_init_nest_lock](../../../parallel/openmp/reference/omp-init-nest-lock.md)합니다.

## <a name="remarks"></a>설명

자세한 내용은 [3.2.2 omp_destroy_lock and omp_destroy_nest_lock 함수](../../../parallel/openmp/3-2-2-omp-destroy-lock-and-omp-destroy-nest-lock-functions.md)합니다.

## <a name="example"></a>예제

참조 [omp_init_nest_lock](../../../parallel/openmp/reference/omp-init-nest-lock.md) 사용 하는 예제에 대 한 `omp_destroy_nest_lock`합니다.

## <a name="see-also"></a>참고 항목

[함수](../../../parallel/openmp/reference/openmp-functions.md)