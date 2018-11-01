---
title: 4.1 OMP_SCHEDULE
ms.date: 11/04/2016
ms.assetid: d0dce411-2351-4ee9-a1cc-c0322a58b65c
ms.openlocfilehash: 4731299a4f7203dd01f660ea25bf2f5b58060630
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50432697"
---
# <a name="41-ompschedule"></a>4.1 OMP_SCHEDULE

**OMP_SCHEDULE** 에 적용 됩니다 **에 대 한** 하 고 **에 대 한 병렬** 일정 유형을 가진 지시문 **런타임**합니다. 인식할 수 있는 일정 형식 및 선택적를이 환경 변수를 설정 하 여 런타임 시 이러한 모든 루프에 대 한 일정 유형 및 청크 크기를 설정할 수 있습니다 *chunk_size*합니다.

에 대 한 **에 대 한** 하 고 **에 대 한 병렬** 이외의 일정 유형에 있는 지시문 **런타임**를 **OMP_SCHEDULE** 무시 됩니다. 이 환경 변수에 대 한 기본값은 구현 시 정의 합니다. 경우 선택적 *chunk_size* 설정, 값은 양수 여야 합니다. 하는 경우 *chunk_size* 1의 값으로 가정 하기를 설정 하지 않으면의 경우를 제외 하 고는 **정적** 일정 합니다. 에 대 한는 **정적** 일정을 기본 청크 크기 루프 반복 공간 루프에 적용 되는 스레드의 수로 나눈 값에 설정 됩니다.

예제:

```
setenv OMP_SCHEDULE "guided,4"
setenv OMP_SCHEDULE "dynamic"
```

## <a name="cross-references"></a>교차 참조:

- **에 대 한** 지시문을 참조 하십시오 [2.4.1 섹션](../../parallel/openmp/2-4-1-for-construct.md) 11 페이지입니다.

- **에 대 한 병렬** 지시문을 참조 하십시오 [2.5.1 섹션](../../parallel/openmp/2-5-1-parallel-for-construct.md) 16 페이지입니다.