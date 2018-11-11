---
title: HUGE_VAL, _HUGE
ms.date: 11/04/2016
apiname:
- _HUGE
apilocation:
- msvcrt.dll
apitype: DLLExport
f1_keywords:
- _HUGE
- HUGE_VAL
helpviewer_keywords:
- _HUGE constant
- HUGE_VAL constant
- double value
ms.assetid: 3f044b45-02cd-46b2-b1de-87fd0441dd6a
ms.openlocfilehash: 96b05bc2f7b608c31a12493a4f1b71535b13dc4f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50630089"
---
# <a name="hugeval-huge"></a>HUGE_VAL, _HUGE

## <a name="syntax"></a>구문

```

#include <math.h>

```

## <a name="remarks"></a>설명

`HUGE_VAL`은 표현할 수 있는 가장 큰 double 값입니다. 오류가 발생하면 여러 런타임 수학 함수에 의해 이 값이 반환됩니다. 일부 함수의 경우 -`HUGE_VAL`가 반환됩니다. `HUGE_VAL`이 `_HUGE`로 정의되지만 런타임 수학 함수는 `HUGE_VAL`을 반환합니다. 또한 일관성을 위해 코드에 `HUGE_VAL`를 사용해야 합니다.

## <a name="see-also"></a>참고 항목

[전역 상수](../c-runtime-library/global-constants.md)