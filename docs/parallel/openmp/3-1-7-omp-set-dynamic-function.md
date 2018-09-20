---
title: 3.1.7 omp_set_dynamic 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 1fba961b-b82c-4a1e-ab0f-e4be826e50ab
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 807e5739c571f7aa8e9f723a0a48c8c46f1e6d09
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46441566"
---
# <a name="317-ompsetdynamic-function"></a>3.1.7 omp_set_dynamic 함수

합니다 **omp_set_dynamic** 함수를 사용할지 지역 병렬 실행에 사용 가능한 스레드 수를 동적으로 조정 합니다. 형식은 다음과 같습니다.

```
#include <omp.h>
void omp_set_dynamic(int dynamic_threads);
```

하는 경우 *dynamic_threads* 평가 0이 아닌 값으로 후속 병렬 영역을 실행 하는 데 사용 되는 스레드 수가 조정 될 수 있습니다 자동으로 시스템 리소스를 최대한 활용 하려면 런타임 환경에서. 결과적으로 사용자가 지정 된 스레드 수가 최대 스레드 수입니다. 병렬 영역을 실행 하는 팀의 스레드 수는 병렬 영역 기간에 대 한 고정 된 상태로 및을 보고 합니다 **omp_get_num_threads** 함수입니다.

하는 경우 *dynamic_threads* 평가를 0으로 동적으로 조정 하는 사용 하지 않도록 설정 합니다.

이 함수는 프로그램의 부분에서 호출 하는 경우 위에서 설명한 효과가 있는 합니다 **omp_in_parallel** 함수가 0을 반환 합니다. 프로그램 부분에서 호출 되는 경우 위치는 **omp_in_parallel** 0이 아닌 값을 반환 하는 함수,이 함수의 동작이 정의 되지 않습니다.

에 대 한 호출 **omp_set_dynamic** 보다 우선 합니다 **OMP_DYNAMIC** 환경 변수입니다.

스레드를 동적으로 조정 해야 하는 항목에 대 한 기본 구현 시 정의 됩니다. 결과적으로, 특정 수의 올바른 실행에 대 한 스레드를에 의존 하는 사용자 코드는 동적 스레드 명시적으로 해제 해야 합니다. 구현 스레드 수를 동적으로 조정 하는 기능을 제공 하는 데 필요한 되지만 모든 플랫폼 간의 이식성을 지원 하기 위해 인터페이스를 제공 해야 합니다.

## <a name="cross-references"></a>교차 참조:

- **omp_get_num_threads** 함수를 참조 하세요 [단원 3.1.2](../../parallel/openmp/3-1-2-omp-get-num-threads-function.md) 37 페이지입니다.

- **OMP_DYNAMIC** 환경 변수를 참조 하십시오 [섹션 4.3](../../parallel/openmp/4-3-omp-dynamic.md) 49 페이지입니다.

- **omp_in_parallel** 함수를 참조 하세요 [3.1.6 섹션](../../parallel/openmp/3-1-6-omp-in-parallel-function.md) 38 페이지입니다.