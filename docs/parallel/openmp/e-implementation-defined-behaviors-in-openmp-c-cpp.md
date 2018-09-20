---
title: E. 구현 정의 동작에서 OpenMP C/c + + | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: b8d660ca-9bb3-4b6b-87af-45c67d43a731
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 6e2e8360dbb2c8851a0ac1c09767928703708a97
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46405010"
---
# <a name="e-implementation-defined-behaviors-in-openmp-cc"></a>E. 구현 시 정의 된 동작에서 OpenMP C/c + +

이 부록에는 "구현 시 정의 된"이 api에서를 설명 하는 동작이 요약 되어 있습니다.  각 동작은 다시 상호 참조 하도록 기본 사양에 설명 합니다.

## <a name="remarks"></a>설명

구현을 정의 하 고 해당 동작의 경우 이러한 문서에 필요 하지만이 목록이 불완전할 수 있습니다.

- **스레드 수가:** 병렬 영역 스레드 수를 동적으로 조정 하지 않으면 스레드 병렬 영역에 대 한 요청 수가 런타임 시스템을 제공할 수 있도록 동작의 수를 초과 하면 하는 동안 발생 한 경우 프로그램은 구현 시 정의 (9 페이지 참조).

     Visual c + +에서는 중첩 되지 않은 병렬 영역에 대 한 64 개 스레드 (최대) 제공 됩니다.

- **프로세서 수가:** 실제로 스레드가 언제 든 지 호스팅하는 실제 프로세서 수는 구현 시 정의 (10 페이지 참조).

     Visual c + +에서는이 숫자 상수 되지 않으며 운영 체제에 의해 제어 됩니다.

- **스레드의 팀 만들기:** 중첩 된 병렬 영역을 실행 하는 팀의 스레드 수가 구현 시 정의 됩니다. ( 10 페이지 참조).

     Visual c + +에서는 운영 체제에 의해 결정 됩니다.

- **schedule (runtime):** 런타임까지 지연 됩니다에 관한 일정 결정 합니다. 일정 유형 및 청크 크기를 설정 하 여 런타임 시 선택할 수 있습니다는 `OMP_SCHEDULE` 환경 변수입니다. 이 환경 변수를 설정 하지 않으면 결과 일정은 구현 시 정의 (13 페이지 참조).

     일정 유형에서는 Visual c + + `static` 청크 크기를 사용 하 여 합니다.

- **기본 일정:** schedule 절의 없는 경우, 기본 일정은 구현 시 정의 (13 페이지 참조).

     Visual c + +에서는 기본 일정 유형은 `static` 청크 크기를 사용 하 여 합니다.

- **ATOMIC:** 것이 구현에서 정의 된 구현을 모두 대체 여부 `atomic` 사용 하 여 지시문 **중요 한** (20 페이지 참조) 동일한 고유 이름을 가진 지시문입니다.

     Visual c + +에서는 수정 된 데이터 [원자성](../../parallel/openmp/reference/atomic.md) 자연 맞춤 켜져 있지 않으면 해당 속성을 만족 하는 모든 장기 원자성 작업 한 중요 한 섹션을 사용할 경우 1 또는 2 바이트입니다. 그렇지 않으면 임계 섹션 사용 되지 않습니다.

- **omp_get_num_threads:** 사용자가 스레드 수를 명시적으로 설정 된에, 경우 기본값은 구현 시 정의 (9 페이지를 참조 및 [단원 3.1.2](../../parallel/openmp/3-1-2-omp-get-num-threads-function.md) 37 페이지).

     Visual c + +에서 기본 스레드 수가 프로세서의 수와 같습니다.

- **omp_set_dynamic:** 동적 스레드 조정에 대 한 기본 구현 시 정의 됩니다 (참조 [3.1.7 섹션](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md) 39 페이지).

     기본값은 Visual c + +에서는 `FALSE`합니다.

- **omp_set_nested:** 중첩 된 병렬 처리를 사용 하는 경우 중첩 된 병렬 영역을 실행 하는 데 사용 되는 스레드의 수는 구현 시 정의 (참조 [3.1.9 섹션](../../parallel/openmp/3-1-9-omp-set-nested-function.md) 40 페이지).

     Visual c + +에서 스레드 수는 운영 체제에 의해 결정 됩니다.

- `OMP_SCHEDULE` 환경 변수:이 환경 변수에 대 한 기본값은 구현 시 정의 (참조 [섹션 4.1](../../parallel/openmp/4-1-omp-schedule.md) 48 페이지).

     일정 유형에서는 Visual c + + `static` 청크 크기를 사용 하 여 합니다.

- `OMP_NUM_THREADS` 환경 변수: 없음 값을 지정 하는 경우는 `OMP_NUM_THREADS` 환경 변수 또는 지정 된 값이 양의 정수 아니거나 값 보다 크면 시스템에서 지원할 수 스레드의 최대 수를 사용 하는 스레드 수 구현 시 정의 (참조 [4.2 섹션](../../parallel/openmp/4-2-omp-num-threads.md) 48 페이지).

     Visual c + +에서는 값을 지정 하는 경우 0 이거나, 스레드 수는 프로세서의 수와 같습니다.  값이 64 보다 크면 스레드 수가 64입니다.

- `OMP_DYNAMIC` 환경 변수: 기본값은 구현 시 정의 (참조 [섹션 4.3](../../parallel/openmp/4-3-omp-dynamic.md) 49 페이지).

     기본값은 Visual c + +에서는 `FALSE`합니다.