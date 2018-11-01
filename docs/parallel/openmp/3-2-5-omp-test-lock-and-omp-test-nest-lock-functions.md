---
title: 3.2.5 omp_test_lock and omp_test_nest_lock 함수
ms.date: 11/04/2016
ms.assetid: 36818945-c22c-4c24-b754-4e73eba6f3f8
ms.openlocfilehash: e8e03699f807f23f139075560592d8846467f2c5
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50512753"
---
# <a name="325-omptestlock-and-omptestnestlock-functions"></a>3.2.5 omp_test_lock and omp_test_nest_lock 함수

이러한 함수는 잠금을 설정 하려고 하지만 스레드 실행을 차단 하지 않습니다. 형식은 다음과 같습니다.

```
#include <omp.h>
int omp_test_lock(omp_lock_t *lock);
int omp_test_nest_lock(omp_nest_lock_t *lock);
```

인수는 초기화 잠금 변수를 가리켜야 합니다. 이러한 함수를 동일한 방식으로 잠금을 설정 하려고 `omp_set_lock` 고 `omp_set_nest_lock`한다는 점을 제외 하는 스레드의 실행을 차단 하지 않습니다.

간단한 잠금에 대 한는 `omp_test_lock` 잠금을 성공적으로 설정 된 경우 함수는 0이 아닌 값을 반환, 그렇지 않으면 0을 반환 합니다.

중첩 가능 잠금는 `omp_test_nest_lock` 함수 잠금을 성공적으로 설정 된 경우 새 중첩 수를 반환, 그렇지 않으면 0을 반환 합니다.