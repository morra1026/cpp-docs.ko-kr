---
title: 3.1.3 omp_get_max_threads 함수
ms.date: 11/04/2016
ms.assetid: 5548897c-546e-4d19-b37b-a76f6b30a0a9
ms.openlocfilehash: 3f954b5ad75b4bdb4a74323f2ab4e819850269ed
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50546586"
---
# <a name="313-ompgetmaxthreads-function"></a>3.1.3 omp_get_max_threads 함수

합니다 **omp_get_max_threads** 이상 만큼 클 경우 병렬 영역 없이 팀을 구성 하는 데 사용할 스레드의 수에 보장 되는 정수를 반환 하는 함수는 **num_threads** 절 코드에서 해당 지점에서 경험할 수 있었습니다. 형식은 다음과 같습니다.

```
#include <omp.h>
int omp_get_max_threads(void);
```

다음 값의 하한값을 표현 **omp_get_max_threads**:

```

threads-used-for-next-team
<= omp_get_max_threads

```

후속 병렬 영역 사용 하는 경우는 **num_threads** 특정 개수의 스레드를 결과 대 한 하한값 대 한 보장을 요청 하는 절 **omp_get_max_threads** 긴 포함 되지 않습니다.

합니다 **omp_get_max_threads** 후속 병렬 영역에서 형성 된 팀의 모든 스레드에 대 한 충분 한 저장소를 동적으로 할당할 함수의 반환 값을 사용할 수 있습니다.

## <a name="cross-references"></a>교차 참조:

- **omp_get_num_threads** 함수를 참조 하세요 [단원 3.1.2](../../parallel/openmp/3-1-2-omp-get-num-threads-function.md) 37 페이지입니다.

- **omp_set_num_threads** 함수를 참조 하세요 [3.1.1 섹션](../../parallel/openmp/3-1-1-omp-set-num-threads-function.md) 36 페이지입니다.

- **omp_set_dynamic** 함수를 참조 하세요 [3.1.7 섹션](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md) 39 페이지입니다.

- **num_threads** 절을 참조 하세요 [섹션 2.3](../../parallel/openmp/2-3-parallel-construct.md) 8 페이지입니다.