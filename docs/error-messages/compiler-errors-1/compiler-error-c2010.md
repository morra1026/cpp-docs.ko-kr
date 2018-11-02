---
title: 컴파일러 오류 C2010
ms.date: 11/04/2016
f1_keywords:
- C2010
helpviewer_keywords:
- C2010
ms.assetid: 5795ed1d-e206-410b-b7b4-528d125c67b4
ms.openlocfilehash: 71cb0012f5e7bda3a0f1409fe71649a5bd0944b8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50434227"
---
# <a name="compiler-error-c2010"></a>컴파일러 오류 C2010

'character': 매크로 정식 매개 변수 목록에 예기치 않은

매크로 정의의 정식 매개 변수 목록에서 문자가 잘못 사용되었습니다. 오류를 해결 하려면 해당 문자를 제거 합니다.

다음 샘플에서는 C2010 오류가 생성 됩니다.

```
// C2010.cpp
// compile with: /c
#define mymacro(a|) (2*a)   // C2010
#define mymacro(a) (2*a)   // OK
```