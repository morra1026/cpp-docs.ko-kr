---
title: 3.1.1 omp_set_num_threads 함수
ms.date: 11/04/2016
ms.assetid: b94cf2b5-8011-4a3b-ba56-676982642857
ms.openlocfilehash: 20b6b6ced2b4031696f1d019604842ae9b91bda2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50663283"
---
# <a name="311-ompsetnumthreads-function"></a>3.1.1 omp_set_num_threads 함수

합니다 `omp_set_num_threads` 기본 지정 하지 않는 후속 병렬 영역에 사용할 스레드 수를 설정 하는 함수를 `num_threads` 절. 형식은 다음과 같습니다.

```
#include <omp.h>
void omp_set_num_threads(int num_threads);
```

매개 변수의 *num_threads* 양의 정수 여야 합니다. 미치는은 스레드 수를 동적으로 조정 활성화 되어 있는지 여부에 따라 다릅니다. 다양 한 간의 상호 작용에 대 한 규칙에 대 한는 `omp_set_num_threads` 함수 및 스레드, 동적으로 조정 8 페이지 섹션 2.3을 참조 하세요.

이 함수는 프로그램의 부분에서 호출 하는 경우 위에서 설명한 효과가 있는 `omp_in_parallel` 함수가 0을 반환 합니다. 프로그램 부분에서 호출 되는 경우 여기서는 `omp_in_parallel` 0이 아닌 값을 반환 하는 함수,이 함수의 동작이 정의 되지 않습니다.

이 호출 보다 우선 합니다 `OMP_NUM_THREADS` 환경 변수입니다. 호출 하 여 설정할 수 있는 스레드의 수에 대 한 기본값 `omp_set_num_threads` 하거나 설정 하는 `OMP_NUM_THREADS` 단일 환경 변수를 명시적으로 재정의할 수 있습니다 **병렬** 지정 하 여 지시문는 `num_threads` 절.

## <a name="cross-references"></a>교차 참조:

- `omp_set_dynamic` 함수를 참조 하세요 [3.1.7 섹션](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md) 39 페이지입니다.

- `omp_get_dynamic` 함수를 참조 하세요 [3.1.8 섹션](../../parallel/openmp/3-1-8-omp-get-dynamic-function.md) 40 페이지입니다.

- `OMP_NUM_THREADS` 환경 변수를 참조 하십시오 [4.2 섹션](../../parallel/openmp/4-2-omp-num-threads.md) 48 페이지와 섹션 2.3 8 페이지에 있습니다.

- `num_threads` 절을 참조 하세요 [섹션 2.3](../../parallel/openmp/2-3-parallel-construct.md) 8 페이지