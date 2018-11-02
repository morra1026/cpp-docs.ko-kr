---
title: 컴파일러 오류 C2013
ms.date: 11/04/2016
f1_keywords:
- C2013
helpviewer_keywords:
- C2013
ms.assetid: 6b5c955c-53da-48ee-8533-64ef5b905173
ms.openlocfilehash: b279202b8b32197a99d230040207aa50bc100495
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50618480"
---
# <a name="compiler-error-c2013"></a>컴파일러 오류 C2013

'>'가 없습니다.

`#include` 지시문에 닫는 꺾쇠 괄호가 없습니다. 오류를 해결하려면 닫는 대괄호를 추가합니다.

다음 샘플에서는 C2013을 생성합니다.

```
// C2013.cpp
#include <stdio.h    // C2013
```

해결 방법:

```
// C2013b.cpp
// compile with: /c
#include <stdio.h>
```