---
title: 컴파일러 오류 C2849
ms.date: 11/04/2016
f1_keywords:
- C2849
helpviewer_keywords:
- C2849
ms.assetid: e28f6b3e-e0e7-4f92-b006-ebaa81d368e6
ms.openlocfilehash: 4812c836d099e9cbb3849e48046edfdeda24ffc9
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50594703"
---
# <a name="compiler-error-c2849"></a>컴파일러 오류 C2849

'소멸자': 인터페이스는 소멸자를 사용할 수 없습니다.

Visual c + + [인터페이스](../../cpp/interface.md) 소멸자를 가질 수 없습니다.

다음 샘플에서는 C2849 오류가 생성 됩니다.

```
// C2849.cpp
// compile with: /c
__interface C {
   ~C();   // C2849 destructor not allowed in an interface
};
```