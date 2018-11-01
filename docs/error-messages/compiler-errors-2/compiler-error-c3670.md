---
title: 컴파일러 오류 C3670
ms.date: 11/04/2016
f1_keywords:
- C3670
helpviewer_keywords:
- C3670
ms.assetid: d0fa9c6e-8f90-48c7-9066-31b4fa5942eb
ms.openlocfilehash: d3acfd9d4d09c53fac0b2c5a2462c56dfd54e6d8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50598551"
---
# <a name="compiler-error-c3670"></a>컴파일러 오류 C3670

'override': 액세스할 수 없는 기본 클래스 ' method'를 재정의할 수 없습니다.

재정의 해당 액세스 수준에 따라 파생된 형식에서 사용할 수 있는 함수만을 시에만 사용할 수 있습니다. 자세한 내용은 [명시적으로 재정의](../../windows/explicit-overrides-cpp-component-extensions.md)합니다.

다음 샘플에서는 C3670 오류가 생성 됩니다.

```
// C3670.cpp
// compile with: /clr /c
public ref class C {
// Uncomment the following line to resolve.
// public:
   virtual void g() { }
};

public ref class D : public C {
public:
   virtual void f() new sealed = C::g {};   // C3670
};
```