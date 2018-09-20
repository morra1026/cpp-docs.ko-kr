---
title: 4.2 OMP_NUM_THREADS | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 49dd55dd-25d5-4a5a-a998-cc7f47b2dae2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9996a09661d962eb5e936fdb484c9dd534e46904
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46445193"
---
# <a name="42-ompnumthreads"></a>4.2 OMP_NUM_THREADS

합니다 **OMP_NUM_THREADS** 환경 변수 해당 숫자를 호출 하 여 명시적으로 변경 하지 않으면 스레드 실행 중에 사용할 기본 개수를 설정 합니다 **omp_set_num_threads** 라이브러리 루틴 또는 명시적 **num_threads** 절에는 **병렬** 지시문입니다.

값을 **OMP_NUM_THREADS** 환경 변수는 양의 정수 여야 합니다. 미치는은 스레드 수를 동적으로 조정 활성화 되어 있는지 여부에 따라 다릅니다. 포괄적인 간의 상호 작용에 대 한 규칙에 대 한 합니다 **OMP_NUM_THREADS** 환경 변수 및 동적 조정 스레드 8 페이지 섹션 2.3을 참조 하세요.

없는 값을 지정 하는 경우는 **OMP_NUM_THREADS** 환경 변수를 지정 된 값을 양의 정수가 아닙니다. 또는 시스템 수 값이 스레드의 최대 수를 초과 하는 경우 또는 지원에 사용할 스레드 수 구현 시 정의 됩니다.

예제:

```
setenv OMP_NUM_THREADS 16
```

## <a name="cross-references"></a>교차 참조:

- **num_threads** 절을 참조 하세요 [섹션 2.3](../../parallel/openmp/2-3-parallel-construct.md) 8 페이지입니다.

- **omp_set_num_threads** 함수를 참조 하세요 [3.1.1 섹션](../../parallel/openmp/3-1-1-omp-set-num-threads-function.md) 36 페이지입니다.

- **omp_set_dynamic** 함수를 참조 하세요 [3.1.7 섹션](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md) 39 페이지입니다.