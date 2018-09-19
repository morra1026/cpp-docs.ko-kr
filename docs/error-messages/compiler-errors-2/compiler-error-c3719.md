---
title: 컴파일러 오류 C3719 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3719
dev_langs:
- C++
helpviewer_keywords:
- C3719
ms.assetid: d0d59d4e-babb-4480-9ef7-70cf1a28165c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 04761008bd7dcdfa9ecb8dc1d6c24be4a67a6360
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46047865"
---
# <a name="compiler-error-c3719"></a>컴파일러 오류 C3719

'interface': COM 이벤트에 대 한 인터페이스 기반된 이벤트 소스만 사용할 수 있습니다

COM이 아닌 컨텍스트에서 인터페이스를 선언 했습니다.

다음 샘플에서는 C3719 오류가 생성 됩니다.

```
// C3719a.cpp
#define _ATL_ATTRIBUTES 1
#include "atlbase.h"
#include "atlcom.h"

[module(name="MyLibrary", version="1.2", helpfile="MyHelpFile")];

[object]
__interface I {
   HRESULT func1();
};

[event_source(native), coclass]
struct A {
   __event __interface I;   // C3719

   // try the following line instead
   // __event func2();
};

int main() {
}
```

이 오류를 해결 하려면 적용 합니다 [개체](../../windows/object-cpp.md), [coclass](../../windows/coclass.md)를 [event_source](../../windows/event-source.md), 및 [event_receiver](../../windows/event-receiver.md) 하도록 적절 하 게 특성는 COM 인터페이스 클래스를 사용 하는 클래스입니다. 예를 들어:

```
// C3719b.cpp
#define _ATL_ATTRIBUTES 1
#include <atlbase.h>
#include <atlcom.h>

[module(name="xx")];
[object, uuid("00000000-0000-0000-0000-000000000001")]
__interface I {
   HRESULT f();
};

[coclass, event_source(com) , uuid("00000000-0000-0000-0000-000000000002")]
struct MyStruct {
   __event __interface I;
};

[event_receiver(com)]
struct MyStruct2 {
   void f() {
   }
   MyStruct2(I* pB) {
      __hook(&I::f, pB, &MyStruct2::f);
   }
};

int main()
{
}
```