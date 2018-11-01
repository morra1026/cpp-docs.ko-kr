---
title: 3.3.1 omp_get_wtime 함수
ms.date: 11/04/2016
ms.assetid: 90188bd2-c53e-4398-8946-d3ecc92fa0f6
ms.openlocfilehash: 544a1bc9a613a2888cb7c5e68e54fdfae1b1c333
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50460569"
---
# <a name="331-ompgetwtime-function"></a>3.3.1 omp_get_wtime 함수

`omp_get_wtime` 함수 반환 배정밀도 부동 소수점 값 경과 된 벽 시계 시간을 몇 가지 "과거의 지정 시간" 이후의 초 단위입니다.  실제 "시간 이전에" 임의적 이지만를 응용 프로그램의 실행 하는 동안 변경 하지 않도록 보장 됩니다. 형식은 다음과 같습니다.

```
#include <omp.h>
double omp_get_wtime(void);
```

다음 예제에서와 같이 경과 시간을 측정 하는 함수를 사용할 수는 것으로 예상 됩니다.

```
double start;
double end;
start = omp_get_wtime();
... work to be timed ...
end = omp_get_wtime();
printf_s("Work took %f sec. time.\n", end-start);
```

반환 된 시간은 응용 프로그램에 참여 하는 모든 스레드에 대해 전역적으로 일관 되도록 필요가 있는 것으로 "스레드별 times" 이며