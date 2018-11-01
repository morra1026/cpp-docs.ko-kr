---
title: 컴파일러 경고(수준 4) C4487
ms.date: 11/04/2016
f1_keywords:
- C4487
helpviewer_keywords:
- C4487
ms.assetid: 796144cf-cd3c-4edc-b6a4-96192b7eb4f0
ms.openlocfilehash: 743069c0ed3103a2ed8d459def65083146b971e1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50497022"
---
# <a name="compiler-warning-level-4-c4487"></a>컴파일러 경고(수준 4) C4487

'derived_class_function': 상속 된 비가상 메서드 'base_class_function'는 일치 하지만 명시적으로 표시 되어 있지 않습니다 'new'

파생된 클래스에서 함수는 비가상 기본 클래스 함수 서명이 동일 합니다. C4487 파생된 클래스는 기본 클래스 함수를 재정의 하지 않습니다를 알려 줍니다. 파생된 클래스 함수를 명시적으로 표시 `new` 이 경고를 해결 하려면.

자세한 내용은 [new (의 new 슬롯 vtable)](../../windows/new-new-slot-in-vtable-cpp-component-extensions.md)합니다.

## <a name="example"></a>예제

다음 샘플 C4487를 생성합니다.

```
// C4487.cpp
// compile with: /W4 /clr
using namespace System;
public ref struct B {
   void f() { Console::WriteLine("in B::f"); }
   void g() { Console::WriteLine("in B::g"); }
};

public ref struct D : B {
   void f() { Console::WriteLine("in D::f"); }   // C4487
   void g() new { Console::WriteLine("in D::g"); }   // OK
};

int main() {
   B ^ a = gcnew D;
   // will call base class functions
   a->f();
   a->g();
}
```