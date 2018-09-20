---
title: 3.1.9 omp_set_nested 함수 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: e4afc3aa-bb96-4314-9849-fd5df5f437d9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 68e5898b8b57814a152ca2ce9ced84a9df8190cc
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46414541"
---
# <a name="319-ompsetnested-function"></a>3.1.9 omp_set_nested 함수

합니다 **omp_set_nested** 함수 하거나 중첩 된 병렬 처리를 사용 하지 않도록 설정 합니다. 형식은 다음과 같습니다.

```
#include <omp.h>
void omp_set_nested(int nested);
```

경우 *중첩 된* 중첩 0으로 계산 되는 기본적으로 병렬 처리 해제 되 고 중첩 된 병렬 영역은 직렬화 되 고 현재 스레드에서 실행 합니다. 하는 경우 *중첩 된* 평가 0이 아닌 값으로 중첩 된 병렬 처리 사용 하 고 중첩 된 병렬 영역 중첩된 팀을 구성 하기 위한 추가 스레드도 배포할 수 있습니다.

이 함수는 프로그램의 부분에서 호출 하는 경우 위에서 설명한 효과가 있는 합니다 **omp_in_parallel** 함수가 0을 반환 합니다. 프로그램 부분에서 호출 되는 경우 위치는 **omp_in_parallel** 0이 아닌 값을 반환 하는 함수,이 함수의 동작이 정의 되지 않습니다.

이 호출 보다 우선 합니다 **OMP_NESTED** 환경 변수입니다.

중첩 된 병렬 처리를 사용 하는 경우 중첩 된 병렬 영역을 실행 하는 데 사용 되는 스레드 수가 구현이 정의 됩니다. 결과적으로, OpenMP 규격 구현 중첩 된 병렬 처리 사용 하도록 설정 하는 경우에 중첩 된 병렬 영역을 serialize 할 수 있습니다.

## <a name="cross-references"></a>교차 참조:

- **OMP_NESTED** 환경 변수를 참조 하십시오 [섹션 4.4](../../parallel/openmp/4-4-omp-nested.md) 49 페이지입니다.

- **omp_in_parallel** 함수를 참조 하세요 [3.1.6 섹션](../../parallel/openmp/3-1-6-omp-in-parallel-function.md) 38 페이지입니다.