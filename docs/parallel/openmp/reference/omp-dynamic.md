---
title: OMP_DYNAMIC | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- OMP_DYNAMIC
dev_langs:
- C++
helpviewer_keywords:
- OMP_DYNAMIC OpenMP environment variable
ms.assetid: e306049d-b644-4b73-8b63-46c835bff98b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: b02a2a4d660057ab83da39add7fd32bcff3e6d90
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46392140"
---
# <a name="ompdynamic"></a>OMP_DYNAMIC

런타임에 OpenMP 병렬 영역에서 스레드 수를 조정할 수 있는지 여부를 지정 합니다.

## <a name="syntax"></a>구문

```
set OMP_DYNAMIC[=TRUE | =FALSE]
```

## <a name="remarks"></a>설명

합니다 `OMP_DYNAMIC` 환경 변수 재정의 될 수 있습니다 합니다 [omp_set_dynamic](../../../parallel/openmp/reference/omp-set-dynamic.md) 함수입니다.

OpenMP 표준의 Visual c + + 구현에서 기본값은 `OMP_DYNAMIC=FALSE`합니다.

자세한 내용은 [4.3 OMP_DYNAMIC](../../../parallel/openmp/4-3-omp-dynamic.md)합니다.

## <a name="example"></a>예제

다음 명령 집합을 `OMP_DYNAMIC` 로 환경 변수:

```
set OMP_DYNAMIC=TRUE
```

다음 명령은의 현재 설정을 표시는 `OMP_DYNAMIC` 환경 변수:

```
set OMP_DYNAMIC
```

## <a name="see-also"></a>참고 항목

[환경 변수](../../../parallel/openmp/reference/openmp-environment-variables.md)