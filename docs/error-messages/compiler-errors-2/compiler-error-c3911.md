---
title: 컴파일러 오류 C3911
ms.date: 11/04/2016
f1_keywords:
- C3911
helpviewer_keywords:
- C3911
ms.assetid: b786da59-0e99-479d-bc0d-551126e940f2
ms.openlocfilehash: 6c00a3bb388130d9a570e9fd731a9ed1200ed179
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50622185"
---
# <a name="compiler-error-c3911"></a>컴파일러 오류 C3911

'event_accessor_method': 함수에는 형식 '서명' 있어야 합니다.

이벤트의 접근자 메서드를 제대로 선언 되지 않았습니다.

자세한 내용은 [이벤트](../../windows/event-cpp-component-extensions.md)합니다.

다음 샘플에서는 C3911 오류가 생성 됩니다.

```
// C3911.cpp
// compile with: /clr
using namespace System;
delegate void H(String^, int);

ref class X {
   event H^ E1 {
      void add() {}   // C3911
      // try the following line instead
      // void add(H ^ h) {}

      void remove(){}
      // try the following line instead
      // void remove(H ^ h) {}

      void raise(){}
      // try the following line instead
      // void raise(String ^ s, int i) {}
   };
};
```