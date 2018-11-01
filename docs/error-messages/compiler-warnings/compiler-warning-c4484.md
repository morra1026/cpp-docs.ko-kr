---
title: 컴파일러 경고 C4484
ms.date: 11/04/2016
f1_keywords:
- C4484
helpviewer_keywords:
- C4484
ms.assetid: 3d30e5b3-2297-45b7-a37a-1360056fdd0e
ms.openlocfilehash: 71a3d903ba32fecac4b2d8bfc3e0a93f19d0f4ed
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50473175"
---
# <a name="compiler-warning-c4484"></a>컴파일러 경고 C4484

'override_function': 기본 ref 클래스 메서드 'base_class_function'는 일치 하지만 'virtual', 'new' 또는 'override'; 표시 되어 있지 않습니다 'new' (및 'virtual' 아님) 가정

사용 하 여 컴파일하면 **/clr**는 컴파일러가 함수 vtable의 new 슬롯 받을 것을 의미 하는 기본 클래스 함수를 암시적으로 재정의 되지 않습니다. 를 해결 하려면 명시적으로 함수를 재정의 인지 여부를 지정 합니다.

자세한 내용은 다음을 참조하세요.

- [/clr(공용 언어 런타임 컴파일)](../../build/reference/clr-common-language-runtime-compilation.md)

- [override](../../windows/override-cpp-component-extensions.md)

- [new (의 new 슬롯 vtable)](../../windows/new-new-slot-in-vtable-cpp-component-extensions.md)

C4484은 항상 오류로 실행 됩니다. 사용 된 [경고](../../preprocessor/warning.md) C4484 표시 하지 않으려면 pragma입니다.

## <a name="example"></a>예제

다음 샘플 C4484를 생성합니다.

```
// C4484.cpp
// compile with: /clr
ref struct A {
   virtual void Test() {}
};

ref struct B : A {
   void Test() {}   // C4484
};

// OK
ref struct C {
   virtual void Test() {}
   virtual void Test2() {}
};

ref struct D : C {
   virtual void Test() new {}
   virtual void Test2() override {}
};
```