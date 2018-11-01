---
title: 3.1.10 omp_get_nested 함수
ms.date: 11/04/2016
ms.assetid: 48736a25-5c6e-4e2d-aad0-421087663a3c
ms.openlocfilehash: a4db1e21f344f5cc58e2027b0816f9c8fb40b3bc
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50519923"
---
# <a name="3110-ompgetnested-function"></a>3.1.10 omp_get_nested 함수

`omp_get_nested` 비활성화 된 경우 함수는 중첩 된 병렬 처리를 사용 하는 경우 0이 아닌 값 및 0 반환 합니다. 중첩 된 병렬 처리에 대 한 자세한 내용은 40 페이지 3.1.9 섹션을 참조 하세요. 형식은 다음과 같습니다.

```
#include <omp.h>
int omp_get_nested(void);
```

구현에서 중첩 된 병렬 처리를 구현 하지 않으면,이 함수는 항상 0을 반환 합니다.