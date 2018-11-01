---
title: 3.1.8 omp_get_dynamic 함수
ms.date: 11/04/2016
ms.assetid: c03e2daf-29c9-49e3-9b67-b980ad1ab195
ms.openlocfilehash: d9476894e5aff4cc7bb9c67fbbeb14d185b65f5e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50566428"
---
# <a name="318-ompgetdynamic-function"></a>3.1.8 omp_get_dynamic 함수

합니다 **omp_get_dynamic** 스레드를 동적으로 조정 사용 하 고 그렇지 않으면 0을 반환 하는 경우 함수는 0이 아닌 값을 반환 합니다. 형식은 다음과 같습니다.

```
#include <omp.h>
int omp_get_dynamic(void);
```

구현에는 스레드 수를 동적으로 조정 구현 하지 않으면,이 함수는 항상 0을 반환 합니다.

## <a name="cross-references"></a>교차 참조:

- 동적 스레드 조정에 대 한 참조 [3.1.7 섹션](../../parallel/openmp/3-1-7-omp-set-dynamic-function.md) 39 페이지입니다.