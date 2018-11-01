---
title: 3.1.2 omp_get_num_threads 함수
ms.date: 11/04/2016
ms.assetid: bcdd76e2-d96b-4884-ac8f-e55fc0c42801
ms.openlocfilehash: 587b49f70896bcfe8c1a805a4ebb13a11e9bb7d0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50465249"
---
# <a name="312-ompgetnumthreads-function"></a>3.1.2 omp_get_num_threads 함수

합니다 **omp_get_num_threads** 함수의 수를 반환 스레드의 현재 호출 하는 병렬 영역을 실행 하는 팀에서. 형식은 다음과 같습니다.

```
#include <omp.h>
int omp_get_num_threads(void);
```

**num_threads** 절을 **omp_set_num_threads** 함수 및 **OMP_NUM_THREADS** 팀의 스레드 수를 제어 하는 환경 변수입니다.

스레드 수가 사용자가 명시적으로 설정 하지는, 기본 구현을 정의 됩니다. 이 함수에서 가장 가까운 바깥쪽 바인딩할 **병렬** 지시문입니다. Serialize 되는 중첩 된 병렬 영역 또는 프로그램의 직렬 부분에서 호출 되 면이 함수는 1을 반환 합니다.

## <a name="cross-references"></a>교차 참조:

- **OMP_NUM_THREADS** 환경 변수를 참조 하십시오 [4.2 섹션](../../parallel/openmp/4-2-omp-num-threads.md) 48 페이지입니다.

- **num_threads** 절을 참조 하세요 [섹션 2.3](../../parallel/openmp/2-3-parallel-construct.md) 8 페이지입니다.

- **병렬** 생성을 참조 하십시오 [섹션 2.3](../../parallel/openmp/2-3-parallel-construct.md) 8 페이지입니다.