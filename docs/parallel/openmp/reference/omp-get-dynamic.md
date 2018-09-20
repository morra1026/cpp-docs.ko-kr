---
title: omp_get_dynamic | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- omp_get_dynamic
dev_langs:
- C++
helpviewer_keywords:
- omp_get_dynamic OpenMP function
ms.assetid: efa843c5-7266-4a75-8db3-22992663d9db
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c2b5a285ef019cd1752b60065f7040d9a937ce38
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46389891"
---
# <a name="ompgetdynamic"></a>omp_get_dynamic

런타임에서 후속 병렬 영역에서 사용할 수 있는 스레드 수를 조정할 수 있으면 여부를 나타내는 값을 반환 합니다.

## <a name="syntax"></a>구문

```
int omp_get_dynamic();
```

## <a name="return-value"></a>반환 값

0이 아닌 경우 스레드를 동적으로 조정 사용 됩니다.

## <a name="remarks"></a>설명

지정 된 스레드를 동적으로 조정 [omp_set_dynamic](../../../parallel/openmp/reference/omp-set-dynamic.md) 하 고 [OMP_DYNAMIC](../../../parallel/openmp/reference/omp-dynamic.md)합니다.

자세한 내용은 [3.1.7 omp_set_dynamic 함수](../../../parallel/openmp/3-1-7-omp-set-dynamic-function.md)합니다.

## <a name="example"></a>예제

참조 [omp_set_dynamic](../../../parallel/openmp/reference/omp-set-dynamic.md) 사용 하는 예제에 대 한 `omp_get_dynamic`합니다.

## <a name="see-also"></a>참고 항목

[함수](../../../parallel/openmp/reference/openmp-functions.md)