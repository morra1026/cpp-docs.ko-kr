---
title: OpenMP 환경 변수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
dev_langs:
- C++
ms.assetid: 2178ce2b-ffa1-45ec-a455-64437711d15d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 98b61535fd07066c4a1ee24658fdfe81047efc90
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46446571"
---
# <a name="openmp-environment-variables"></a>OpenMP 환경 변수

OpenMP API에서 사용 되는 환경 변수를 제공 합니다.

표준 OpenMP의 Visual c + + 구현에는 다음 환경 변수를 포함 합니다. 이러한 환경 변수는 프로그램 시작 시 읽고 수정 값으로는 런타임 시 무시 됩니다 (예를 들어,를 사용 하 여 [_putenv, _wputenv](../../../c-runtime-library/reference/putenv-wputenv.md)).

|환경 변수|설명|
|--------------------------|-----------------|
|[OMP_DYNAMIC](../../../parallel/openmp/reference/omp-dynamic.md)|런타임에 OpenMP 병렬 영역에서 스레드 수를 조정할 수 있는지 여부를 지정 합니다.|
|[OMP_NESTED](../../../parallel/openmp/reference/omp-nested.md)|중첩 된 병렬 처리 사용 하도록 설정 하거나 해제 되는 경우가 아니면 중첩 된 병렬 처리는 사용 여부를 지정 `omp_set_nested`합니다.|
|[OMP_NUM_THREADS](../../../parallel/openmp/reference/omp-num-threads.md)|의해 재정의 되지 않는 병렬 지역의 스레드의 최대 수를 설정 [omp_set_num_threads](../../../parallel/openmp/reference/omp-set-num-threads.md) 하거나 [num_threads](../../../parallel/openmp/reference/num-threads.md)합니다.|
|[OMP_SCHEDULE](../../../parallel/openmp/reference/omp-schedule.md)|동작을 수정 합니다 [일정](../../../parallel/openmp/reference/schedule.md) 절 때 `schedule(runtime)` 에 지정 된을 `for` 또는 `parallel for` 지시문입니다.|

## <a name="see-also"></a>참고 항목

[라이브러리 참조](../../../parallel/openmp/reference/openmp-library-reference.md)