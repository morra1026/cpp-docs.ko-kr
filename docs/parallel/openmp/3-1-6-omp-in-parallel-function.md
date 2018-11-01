---
title: 3.1.6 omp_in_parallel 함수
ms.date: 11/04/2016
ms.assetid: db6e3a63-2a0a-4b8e-8cc6-c6b49edca5fb
ms.openlocfilehash: 2f251cb994771278c7f4e3f50f01e02126f6f88d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50482045"
---
# <a name="316-ompinparallel-function"></a>3.1.6 omp_in_parallel 함수

합니다 **omp_in_parallel** 병렬로 실행 하는 병렬 영역 동적 범위 내에서 호출 되 면 함수는 0이 아닌 값을 반환, 그렇지 않으면 0을 반환 합니다. 형식은 다음과 같습니다.

```
#include <omp.h>
int omp_in_parallel(void);
```

이 함수에는 serialize 되는 중첩 된 영역을 포함 하 여 병렬로 실행 하는 지역 내에서 호출 될 경우 0이 아닌 값을 반환 합니다.