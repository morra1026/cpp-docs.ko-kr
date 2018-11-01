---
title: 3.2.4 omp_unset_lock and omp_unset_nest_lock 함수
ms.date: 11/04/2016
ms.assetid: 5357e43e-a7c0-41d7-b529-3f7d15da8b11
ms.openlocfilehash: b0764e3590f8edb3a3e783d9b5493a64be154401
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50607868"
---
# <a name="324-ompunsetlock-and-ompunsetnestlock-functions"></a>3.2.4 omp_unset_lock and omp_unset_nest_lock 함수

이러한 함수는 잠금 소유권을 해제 하는 수단을 제공 합니다. 형식은 다음과 같습니다.

```
#include <omp.h>
void omp_unset_lock(omp_lock_t *lock);
void omp_unset_nest_lock(omp_nest_lock_t *lock);
```

이러한 각 함수에 대 한 인수는 함수를 실행 하는 스레드를 소유 하는 초기화 잠금 변수를 가리키도록 해야 합니다. 스레드는 잠금을 소유 하지 않는 경우 동작이 정의 되지 않습니다.

간단한 잠금에 대 한는 `omp_unset_lock` 함수 잠금 소유권에서 함수를 실행 하는 스레드를 해제 합니다.

중첩 가능 잠금는 `omp_unset_nest_lock` 함수는 중첩 개수 및 릴리스 결과 횟수가 0 이면 잠금 소유권에서 함수를 실행 하는 스레드입니다.