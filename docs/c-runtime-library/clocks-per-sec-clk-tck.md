---
title: CLOCKS_PER_SEC, CLK_TCK
ms.date: 11/04/2016
f1_keywords:
- CLOCKS_PER_SEC
- CLK_TCK
helpviewer_keywords:
- CLOCKS_PER_SEC
- CLK_TCK constant
ms.assetid: bc285106-383d-44cb-91bf-276ad7de57bf
ms.openlocfilehash: 40401028ef16f0d46baec92a37b2ba422d1e56ae
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50621353"
---
# <a name="clockspersec-clktck"></a>CLOCKS_PER_SEC, CLK_TCK

## <a name="syntax"></a>구문

```

#include <time.h>
```

## <a name="remarks"></a>설명

초 단위 시간은 `clock` 함수에 의해 반환된 값을 `CLOCKS_PER_SEC`로 나눈 값입니다. `CLK_TCK`는 동일하지만 사용되지 않습니다.

## <a name="see-also"></a>참고 항목

[clock](../c-runtime-library/reference/clock.md)<br/>
[전역 상수](../c-runtime-library/global-constants.md)