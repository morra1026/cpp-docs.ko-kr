---
title: 2.3 parallel 구문
ms.date: 11/04/2016
ms.assetid: 190eacdf-2c16-4c06-8cb7-ac60eb211425
ms.openlocfilehash: 6ee7539af05bef1fdca117d806900f2f5a9c0d7f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50494677"
---
# <a name="23-parallel-construct"></a>2.3 parallel 구문

다음 지시문을 동시에 여러 스레드에서 실행할 프로그램의 영역인 병렬 영역을 정의 합니다. 이 병렬 실행을 시작 하는 기본 구문입니다.

```
#pragma omp parallel [clause[ [, ]clause] ...] new-line   structured-block
```

합니다 *절* 다음 중 하나입니다.

**if(** *scalar-expression* **)**

**private(** *variable-list* **)**

**firstprivate(** *variable-list* **)**

**기본 (공유 &#124; 없음)**

**shared(** *variable-list* **)**

**copyin(** *variable-list* **)**

**reduction(** *operator* **:**  *variable-list* **)**

**num_threads(** *integer-expression* **)**

스레드는 병렬 구문에서 발견 하는 경우 다음과 같은 경우 중 하나가 참인 경우 스레드 팀이 만들어집니다.

- 아니오 **경우** 절이 있습니다.

- 합니다 **경우** 식이 0이 아닌 값입니다.

이 스레드가 마스터 스레드는 스레드 번호 0 사용 하 여 팀의 되며 마스터 스레드를 포함 하 여 팀의 모든 스레드 지역을 병렬로 실행 합니다. 하는 경우의 값을 **경우** 식이 0 이면, 지역 serialize 됩니다.

요청 된 스레드의 수를 확인 하려면 다음 규칙 순서로 간주 됩니다. 조건이 충족 될 첫 번째 규칙이 적용 됩니다.

1. 경우는 **num_threads** 절을 사용할 수 있으면 다음 정수 식의 값을 요청 하는 스레드입니다.

1. 경우는 **omp_set_num_threads** 라이브러리 함수를 호출한 다음 가장 최근에 실행된 한 호출의 인수 값은 요청 스레드의 수입니다.

1. 경우 환경 변수 **OMP_NUM_THREADS** 이 환경 변수의 값은 요청 하는 스레드 수가 정의 됩니다.

1. 위의 방법 중 사용한 요청 스레드 수가 경우 구현 시 정의 합니다.

경우는 **num_threads** 절이 있으면 다음 요청한 스레드의 개수를 대체 합니다 **omp_set_num_threads** 라이브러리 함수 또는 **OMP_NUM_THREADS** 환경 변수에서만 병렬 영역에 적용 됩니다. 후속 병렬 영역에서 받지 않습니다.

또한 병렬 영역을 실행 하는 스레드 수가 스레드 수를 동적으로 조정 가능 여부에 따라 달라 집니다. 동적으로 조정 하지 않으면 스레드 수가 요청 된 병렬 영역을 실행 됩니다. 이상을 사용 하는 경우 요청 된 스레드 수는 병렬 영역을 실행할 수 있는 스레드의 최대 수입니다.

병렬 영역 스레드 수를 동적으로 조정 하지 않으면 스레드 병렬 영역에 대 한 요청 수가 런타임 시스템에서 제공할 수 있는 수를 초과 하는 동안 발생 하는 경우 프로그램의 동작은 구현 시 정의 합니다. 구현을 프로그램의 실행을 중단할 예를 들어 수 또는 병렬 영역을 serialize 될 수 있습니다.

합니다 **omp_set_dynamic** 라이브러리 함수 및 **OMP_DYNAMIC** 설정 및 해제 스레드 수를 동적으로 조정 하는 환경 변수를 사용할 수 있습니다.

스레드가 지정된 된 시간에 실제로 호스팅하는 실제 프로세서 수가 구현 시 정의 됩니다. 만들어지면 팀의 스레드 수가 일정 하 게 유지 병렬 영역은 해당 기간에 대 한 합니다. 다른 하나의 병렬 영역에서 런타임 시스템에서 사용자가 명시적으로 또는 자동으로 변경할 수 있습니다.

병렬 영역 동적 범위 내에 포함 된 문은 각 스레드에 의해 실행 됩니다 하 고 각 스레드가 다른 스레드에서 다른 문의 경로 실행할 수 있습니다. 병렬 영역 어휘 범위 외부에서 발생 하는 지시문 분리 된 지시문으로 참조 됩니다.

병렬 영역 끝에는 묵시적된 장벽이 있습니다. 팀의 마스터 스레드만 병렬 영역 끝에 실행을 계속합니다.

병렬 영역을 실행 하는 팀의 스레드가 다른 병렬 구문을 발견 하면, 새 팀을 만들면 및 새 팀에 마스터 서버가 됩니다. 중첩 된 병렬 영역은 기본적으로 serialize 됩니다. 결과적으로, 기본적으로 중첩 된 병렬 영역 중 하나의 구성 하는 팀에서 실행 됩니다. 런타임 라이브러리 함수를 사용 하 여 기본 동작을 변경할 수 있습니다 **omp_set_nested** 환경 변수나 **OMP_NESTED**합니다. 그러나 중첩 된 병렬 영역을 실행 하는 팀의 스레드 수가 구현이 정의 됩니다.

에 대 한 제한 된 **병렬** 지시문은 다음과 같습니다.

- 최대 하나의 **경우** 지시문에 절에 나타날 수 있습니다.

- 효과 경우 내 모든 쪽 여부 지정 되지 않습니다 식 또는 **num_threads** 식 발생 합니다.

- A **throw** 실행 병렬 영역 내에서 같은 구조화 된 블록의 동적 범위 내에서 다시 시작 하려면 실행을 수행 해야 하 고 예외를 발생 시킨 동일한 스레드에서 찾아내야 합니다.

- 단일 **num_threads** 지시문에 절에 나타날 수 있습니다. 합니다 **num_threads** 식 병렬 영역의 컨텍스트 외부에서 평가 되 고 양의 정수 값으로 계산 되어야 합니다.

- 계산 순서를 **하는 경우** 하 고 **num_threads** 절이 지정 되지 않습니다.

## <a name="cross-references"></a>교차 참조:

- **개인**, **firstprivate**, **기본값**를 **공유**, **copyin**, 및 **감소**절을 참조 하세요 [2.7.2 섹션](../../parallel/openmp/2-7-2-data-sharing-attribute-clauses.md) 25 페이지입니다.

- **OMP_NUM_THREADS** 환경 변수 [4.2 섹션](../../parallel/openmp/4-2-omp-num-threads.md) 48 페이지입니다.

- **omp_set_dynamic** 라이브러리 함수를 참조 하세요 [3.1.7 섹션](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md) 39 페이지입니다.

- **OMP_DYNAMIC** 환경 변수를 참조 하십시오 [섹션 4.3](../../parallel/openmp/4-3-omp-dynamic.md) 49 페이지입니다.

- **omp_set_nested** 함수를 참조 하세요 [3.1.9 섹션](../../parallel/openmp/3-1-9-omp-set-nested-function.md) 40 페이지입니다.

- **OMP_NESTED** 환경 변수를 참조 하십시오 [섹션 4.4](../../parallel/openmp/4-4-omp-nested.md) 49 페이지입니다.

- **omp_set_num_threads** 라이브러리 함수를 참조 하세요 [3.1.1 섹션](../../parallel/openmp/3-1-1-omp-set-num-threads-function.md) 36 페이지입니다.