---
title: F. 버전 2.0에서에서 새 기능 및 설명
ms.date: 11/04/2016
ms.assetid: 0d4beb66-f2d5-468c-8cd3-4b00dcbab061
ms.openlocfilehash: c8a597c6af397bd162d92a945d96409b1839e2a3
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50657150"
---
# <a name="f-new-features-and-clarifications-in-version-20"></a>F. 버전 2.0에서에서 새 기능 및 설명

이 부록에는 OpenMP C/c + + 사양 버전 1.0에서에서 2.0 버전으로 이동 하려고 하는 주요 변경 요약 되어 있습니다. 다음 항목은 사양에 추가 하는 새로운 기능:

- 쉼표는 OpenMP 지시문에 허용 됩니다 ([섹션 2.1](../../parallel/openmp/2-1-directive-format.md) 7 페이지).

- 추가 된 `num_threads` 절. 이 절을 사용 하면 특정 개수의 스레드는 병렬 구문에 대 한 요청 수 있습니다 ([섹션 2.3](../../parallel/openmp/2-3-parallel-construct.md) 8 페이지).

- 합니다 `threadprivate` 지시문 정적 블록 범위 변수를 허용 하도록 확장 되었습니다 ([2.7.1 섹션](../../parallel/openmp/2-7-1-threadprivate-directive.md) 23 페이지).

- C99 가변 길이 배열 완전 한 형식이, 및 따라서 지정할 수 있습니다 어디서 나 완전 한 형식이 허용 됩니다, 예를 들어 목록에 `private`하십시오 `firstprivate`, 및 `lastprivate` 절 ([2.7.2 섹션](../../parallel/openmp/2-7-2-data-sharing-attribute-clauses.md) 25 페이지).

- 병렬 영역에서 전용 변수를 중첩 된 지시문에서 다시 개인으로 표시 될 수 있습니다 ([2.7.2.1 섹션](../../parallel/openmp/2-7-2-1-private.md) 25 페이지).

- `copyprivate` 절이 추가 되었습니다. 다른 구성원에 게 팀의 한 멤버에서 값을 브로드캐스트 개인 변수를 사용 하는 메커니즘을 제공 합니다. 경우에 공유 변수를 제공 (예를 들어, 각 수준에서 서로 다른 변수를 요구 하는 재귀)에서 어려운 값에 대 한 공유 변수를 사용 하는 대신 것입니다. 합니다 `copyprivate` 절 에서만 나타날 수 있습니다 합니다 **단일** 지시문 ([2.7.2.8 섹션](../../parallel/openmp/2-7-2-8-copyprivate.md) 32 페이지).

- 또한 타이밍 루틴 `omp_get_wtick` 및 `omp_get_wtime` MPI 루틴 비슷합니다. 이러한 함수는 벽 시계 시간을 수행 하기 위해 필요한 ([3.3.1 단원](../../parallel/openmp/3-3-1-omp-get-wtime-function.md) 44 페이지 및 [섹션 3.3.2](../../parallel/openmp/3-3-2-omp-get-wtick-function.md) 45 페이지).

- 구현 시 정의 된 동작에서 OpenMP C/c + +의 목록이 포함 된 부록도 추가 되었습니다. 구현을 정의 하 고 이러한 경우 해당 동작을 문서화 하는 일을 해야 하는 ([부록 E](../../parallel/openmp/e-implementation-defined-behaviors-in-openmp-c-cpp.md) 97 페이지).

- 다음 변경 내용을 명확 하 게 하거나 수정 C/c + +에 대 한 이전 OpenMP API 사양에는 기능 제공:

   - 한다는 설명이 명확해졌습니다의 동작 `omp_set_nested` 하 고 `omp_set_dynamic` 때 `omp_in_parallel` 0이 아닌 반환이 정의 되지 않습니다 ([3.1.7 섹션](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md) 39 페이지 및 [3.1.9 섹션](../../parallel/openmp/3-1-9-omp-set-nested-function.md) 40 페이지).

   - 중첩 된 병렬 사용 되는 경우 지시문 중첩 설명이 명시 되었습니다 ([2.9 섹션](../../parallel/openmp/2-9-directive-nesting.md) 33 페이지).

   - 병렬 영역 잠금 초기화 및 잠금 소멸 함수를 호출할 수 있습니다 ([3.2.1 섹션](../../parallel/openmp/3-2-1-omp-init-lock-and-omp-init-nest-lock-functions.md) 42 페이지 및 [3.2.2 섹션](../../parallel/openmp/3-2-2-omp-destroy-lock-and-omp-destroy-nest-lock-functions.md) 42 페이지).

   - 새 예제 추가 되었습니다 ([부록 A](../../parallel/openmp/a-examples.md) 51 페이지).