---
title: OpenMP 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
dev_langs:
- C++
ms.assetid: a55a2e5c-a260-44ee-bbd6-de7e2351b384
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: a5daa7737f63df437f31f349a85811befe0c8f5b
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46425602"
---
# <a name="openmp-functions"></a>OpenMP 함수

OpenMP API에서 사용 되는 함수에 대 한 링크를 제공 합니다.

다음 함수를 포함 하는 표준 OpenMP의 Visual c + + 구현 합니다.

|기능|설명|
|--------------|-----------------|
|[omp_destroy_lock](../../../parallel/openmp/reference/omp-destroy-lock.md)|잠금을 초기화를 취소 합니다.|
|[omp_destroy_nest_lock](../../../parallel/openmp/reference/omp-destroy-nest-lock.md)|중첩 가능 잠금을 초기화를 취소 합니다.|
|[omp_get_dynamic](../../../parallel/openmp/reference/omp-get-dynamic.md)|런타임에서 후속 병렬 영역에서 사용할 수 있는 스레드 수를 조정할 수 있으면 여부를 나타내는 값을 반환 합니다.|
|[omp_get_max_threads](../../../parallel/openmp/reference/omp-get-max-threads.md)|있는 경우 병렬 영역 없이 사용할 수 있는 스레드 수보다 크거나 같은 정수를 반환 [num_threads](../../../parallel/openmp/reference/num-threads.md) 코드에서 해당 지점에서 정의 되었습니다.|
|[omp_get_nested](../../../parallel/openmp/reference/omp-get-nested.md)|중첩 된 병렬 처리를 설정할지 여부를 나타내는 값을 반환 합니다.|
|[omp_get_num_procs](../../../parallel/openmp/reference/omp-get-num-procs.md)|함수를 호출할 때 사용할 수 있는 프로세서 수를 반환 합니다.|
|[omp_get_num_threads](../../../parallel/openmp/reference/omp-get-num-threads.md)|병렬 영역에서 스레드 수를 반환합니다.|
|[omp_get_thread_num](../../../parallel/openmp/reference/omp-get-thread-num.md)|해당 스레드 팀 내에서 실행 중인 스레드의 스레드 수를 반환 합니다.|
|[omp_get_wtick](../../../parallel/openmp/reference/omp-get-wtick.md)|프로세서 클록 틱 사이의 시간 (초) 수를 반환합니다.|
|[omp_get_wtime](../../../parallel/openmp/reference/omp-get-wtime.md)|어느 시점에서 경과 된 시간의 초 값을 반환 합니다.|
|[omp_in_parallel](../../../parallel/openmp/reference/omp-in-parallel.md)|병렬 영역 내부에서 호출 된 경우 0이 아닌 값을 반환 합니다.|
|[omp_init_lock](../../../parallel/openmp/reference/omp-init-lock.md)|간단한 잠금을 초기화합니다.|
|[omp_init_nest_lock](../../../parallel/openmp/reference/omp-init-nest-lock.md)|잠금을 초기화합니다.|
|[omp_set_dynamic](../../../parallel/openmp/reference/omp-set-dynamic.md)|런타임에서 후속 병렬 영역에서 사용할 수 있는 스레드 수를 조정할 수 있는지를 나타냅니다.|
|[omp_set_lock](../../../parallel/openmp/reference/omp-set-lock.md)|블록 스레드 잠금을 제공 될 때까지 실행 합니다.|
|[omp_set_nest_lock](../../../parallel/openmp/reference/omp-set-nest-lock.md)|블록 스레드 잠금을 제공 될 때까지 실행 합니다.|
|[omp_set_nested](../../../parallel/openmp/reference/omp-set-nested.md)|중첩 된 병렬 처리가 가능 합니다.|
|[omp_set_num_threads](../../../parallel/openmp/reference/omp-set-num-threads.md)|재정의 되지 않으면 후속 병렬 지역의 스레드 수가 설정 된 [num_threads](../../../parallel/openmp/reference/num-threads.md) 절.|
|[omp_test_lock](../../../parallel/openmp/reference/omp-test-lock.md)|잠금을 설정 하려고 시도 하지만 스레드 실행을 차단 하지 않습니다.|
|[omp_test_nest_lock](../../../parallel/openmp/reference/omp-test-nest-lock.md)|중첩 가능 잠금을 설정 하려고 시도 하지만 스레드 실행을 차단 하지 않습니다.|
|[omp_unset_lock](../../../parallel/openmp/reference/omp-unset-lock.md)|잠금을 해제합니다.|
|[omp_unset_nest_lock](../../../parallel/openmp/reference/omp-unset-nest-lock.md)|중첩 가능 잠금을 해제합니다.|

## <a name="see-also"></a>참고 항목

[라이브러리 참조](../../../parallel/openmp/reference/openmp-library-reference.md)