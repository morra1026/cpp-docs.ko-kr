---
title: 3.2.2 omp_destroy_lock and omp_destroy_nest_lock 함수
ms.date: 11/04/2016
ms.assetid: d334907d-94f7-4bbf-b20e-41d53484cbff
ms.openlocfilehash: 02f739ab2834db7eca9b051e6659644c39b51e84
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50666205"
---
# <a name="322-ompdestroylock-and-ompdestroynestlock-functions"></a>3.2.2 omp_destroy_lock and omp_destroy_nest_lock 함수

이러한 함수 되도록 지정 된 잠금 변수에 *잠금* 초기화 되지 않았습니다. 형식은 다음과 같습니다.

```
#include <omp.h>
void omp_destroy_lock(omp_lock_t *lock);
void omp_destroy_nest_lock(omp_nest_lock_t *lock);
```

초기화 되지 않은 또는 잠금 해제 하는 잠금 변수를 사용 하 여 이러한 루틴 중 하나를 호출 하는 정책을 준수 하지 않는 경우