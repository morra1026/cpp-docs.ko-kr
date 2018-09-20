---
title: default (OpenMP) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- default
dev_langs:
- C++
helpviewer_keywords:
- default OpenMP clause
- defaults, OpenMP clause
ms.assetid: 96055106-a8f0-40b3-8319-e412b6e07bf8
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 4ea32f473d96c8f48c6628d8f71212269bd6d345
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46392616"
---
# <a name="default-openmp"></a>default (OpenMP)

병렬 영역 범위가 지정 되지 않은 변수 동작을 지정 합니다.

## <a name="syntax"></a>구문

```
default(shared | none)
```

## <a name="remarks"></a>설명

`shared`적용 되는 경우는 `default` 절을 지정 하지 않으면으로 지정 된 것 처럼 병렬 영역에서 모든 변수는 처리 함을 의미 합니다 [공유](../../../parallel/openmp/reference/shared-openmp.md) 절. `none` 즉, 병렬 지역으로 범위가 없는 경우에 사용 되는 모든 변수를 [사설](../../../parallel/openmp/reference/private-openmp.md), [공유](../../../parallel/openmp/reference/shared-openmp.md), [감소](../../../parallel/openmp/reference/reduction.md), [firstprivate](../../../parallel/openmp/reference/firstprivate.md), 또는 [lastprivate](../../../parallel/openmp/reference/lastprivate.md) 절 하면 컴파일러 오류가 발생 합니다.

`default` 다음 지시문에 적용 됩니다.

- [parallel](../../../parallel/openmp/reference/parallel.md)

- [for](../../../parallel/openmp/reference/for-openmp.md)

- [섹션](../../../parallel/openmp/reference/sections-openmp.md)

자세한 내용은 [2.7.2.5 기본](../../../parallel/openmp/2-7-2-5-default.md)입니다.

## <a name="example"></a>예제

참조 [사설](../../../parallel/openmp/reference/private-openmp.md) 사용 하는 예제에 대 한 `default`합니다.

## <a name="see-also"></a>참고 항목

[절](../../../parallel/openmp/reference/openmp-clauses.md)