---
title: 컴파일러 오류 C3283
ms.date: 11/04/2016
f1_keywords:
- C3283
helpviewer_keywords:
- C3283
ms.assetid: c51d912c-cde3-4928-904e-26734c8954ce
ms.openlocfilehash: 873ab4d4b016fa392b7a2f64fdd14c3e93f2e22d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50516092"
---
# <a name="compiler-error-c3283"></a>컴파일러 오류 C3283

'type': 인터페이스에는 인스턴스 생성자를 사용할 수 없습니다.

CLR [인터페이스](../../windows/interface-class-cpp-component-extensions.md) 에는 인스턴스 생성자를 사용할 수 없습니다.  정적 생성자는 허용됩니다.

다음 샘플에서는 C3283을 생성합니다.

```
// C3283.cpp
// compile with: /clr
interface class I {
   I();   // C3283
};
```

해결 방법:

```
// C3283b.cpp
// compile with: /clr /c
interface class I {
   static I(){}
};
```