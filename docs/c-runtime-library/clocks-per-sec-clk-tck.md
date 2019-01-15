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
ms.openlocfilehash: a604425809f43be238cbcc7b9148782bb937e00f
ms.sourcegitcommit: a1fad0a266b20b313364a74b16c9ac45d089b1e9
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/11/2019
ms.locfileid: "54220363"
---
# <a name="clockspersec-clktck"></a>CLOCKS_PER_SEC, CLK_TCK

## <a name="syntax"></a>구문

```
#include <time.h>
```

## <a name="remarks"></a>주의

초 단위 시간은 `clock` 함수에 의해 반환된 값을 `CLOCKS_PER_SEC`로 나눈 값입니다. `CLK_TCK`는 동일하지만 사용되지 않습니다.

## <a name="see-also"></a>참고 항목

[clock](../c-runtime-library/reference/clock.md)<br/>
[전역 상수](../c-runtime-library/global-constants.md)
