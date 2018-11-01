---
title: 컴파일러 오류 C3656
ms.date: 11/04/2016
f1_keywords:
- C3656
helpviewer_keywords:
- C3656
ms.assetid: 88965d85-73b0-4b35-8020-0650c9c94cd8
ms.openlocfilehash: 219b8a4135fda963fdce038a75ce0543d6a3433b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50465522"
---
# <a name="compiler-error-c3656"></a>컴파일러 오류 C3656

'override': 재정의 지정자를 반복할 수 없습니다

명시적 재정의 키워드는 한 번만 지정할 수 있습니다. 자세한 내용은 [명시적으로 재정의](../../windows/explicit-overrides-cpp-component-extensions.md)합니다.

다음 샘플에서는 C3656 오류가 생성 됩니다.

```
// C3656.cpp
// compile with: /clr /c
public interface struct O {
   int f();
};

public ref struct V : O {
   int f() override override { return 0; }   // C3656
   // try the following line instead
   // int f() override { return 0; }
};
```