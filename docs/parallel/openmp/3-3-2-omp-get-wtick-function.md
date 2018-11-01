---
title: 3.3.2 omp_get_wtick 함수
ms.date: 11/04/2016
ms.assetid: 1ad08500-bcb0-40d9-a81f-f131819006c9
ms.openlocfilehash: af1e5cf8ef40621342a5162f90cf8c883a59c6a2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50617960"
---
# <a name="332-ompgetwtick-function"></a>3.3.2 omp_get_wtick 함수

`omp_get_wtick` 반환 배정밀도 부동 소수점 값 시간 (초) 수와 같은 연속 클록 틱 간입니다. 형식은 다음과 같습니다.

```
#include <omp.h>
double omp_get_wtick(void);
```