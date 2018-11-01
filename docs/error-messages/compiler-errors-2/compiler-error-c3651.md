---
title: 컴파일러 오류 C3651
ms.date: 11/04/2016
f1_keywords:
- C3651
helpviewer_keywords:
- C3651
ms.assetid: a03e692e-c219-4654-9827-8415cfa5a22d
ms.openlocfilehash: 5601dd2f510e4322e67f49478eefce795312e380
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50494183"
---
# <a name="compiler-error-c3651"></a>컴파일러 오류 C3651

'member': 명시적 재정의로 사용할 수 없습니다, 기본 클래스의 멤버 여야 합니다

명시적 재정의 지정 되었지만 기본 형식이 아닌 형식에서 재정의 된 함수의 되었습니다.

자세한 내용은 [명시적으로 재정의](../../windows/explicit-overrides-cpp-component-extensions.md)합니다.

다음 샘플에서는 C3651 오류가 생성 됩니다.

```
// C3651.cpp
// compile with: /clr /c
ref class C {
public:
   virtual void func2();
};

ref class Other {
public:
   virtual void func();
};

ref class D : public C {
public:
   virtual void func() new sealed = Other::func;   // C3651
   virtual void func2() new sealed = C::func2;   // OK
};
```