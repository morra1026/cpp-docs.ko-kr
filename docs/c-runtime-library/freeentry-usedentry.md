---
title: _FREEENTRY, _USEDENTRY
ms.date: 11/04/2016
f1_keywords:
- USEDENTRY
- _USEDENTRY
- _FREEENTRY
- FREEENTRY
helpviewer_keywords:
- _USEDENTRY constant
- _FREEENTRY constant
- FREEENTRY constant
- USEDENTRY constant
ms.assetid: 26f658e6-6846-4a4e-9984-262cfe392770
ms.openlocfilehash: 3bf05807930373a905a5bf71cf4ebc1f119056a2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50513986"
---
# <a name="freeentry-usedentry"></a>_FREEENTRY, _USEDENTRY

## <a name="syntax"></a>구문

```
#include <malloc.h>
```

## <a name="remarks"></a>설명

이러한 상수는 `_heapwalk` 루틴에 의해 **_HEAPINFO** 구조체의 **_useflag** 요소에 할당된 값을 나타냅니다. 힙 항목의 상태를 나타냅니다.

## <a name="see-also"></a>참고 항목

[_heapwalk](../c-runtime-library/reference/heapwalk.md)<br/>
[전역 상수](../c-runtime-library/global-constants.md)