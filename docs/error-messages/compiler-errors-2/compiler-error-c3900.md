---
title: 컴파일러 오류 C3900
ms.date: 11/04/2016
f1_keywords:
- C3900
helpviewer_keywords:
- C3900
ms.assetid: a94cc561-8fa8-4344-9e01-e81ff462fae5
ms.openlocfilehash: d031b55407d108b4f8be362156911bfae688326a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50512361"
---
# <a name="compiler-error-c3900"></a>컴파일러 오류 C3900

'member': 현재 범위에 사용할 수 없습니다

속성 블록에는 함수 선언 및 인라인 함수 정의 포함 될 수 있습니다. 함수 이외의 멤버가 속성 블록에서 허용 됩니다. Typedef, 연산자 또는 friend 함수가 없는 허용 됩니다. 자세한 내용은 [property](../../windows/property-cpp-component-extensions.md)을 참조하세요.

이벤트 정의 액세스 방법 및 함수에만 포함할 수 있습니다.

다음 샘플에서는 C3900를 생성합니다.

```
// C3900.cpp
// compile with: /clr
ref class X {
   property int P {
      void set(int);   // OK
      int i;   // C3900 variable declaration
   };
};
```

다음 샘플에서는 C3900를 생성합니다.

```
// C3900b.cpp
// compile with: /clr
using namespace System;
delegate void H();
ref class X {
   event H^ E {
      int m;   // C3900

      // OK
      void Test() {}

      void add( H^ h ) {}
      void remove( H^ h ) {}
      void raise( ) {}
   }
};
```