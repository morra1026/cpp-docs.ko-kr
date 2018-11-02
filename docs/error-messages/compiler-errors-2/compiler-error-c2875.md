---
title: 컴파일러 오류 C2875
ms.date: 11/04/2016
f1_keywords:
- C2875
helpviewer_keywords:
- C2875
ms.assetid: d589fc0c-08b2-4a79-bc0e-dca5eb80bdd5
ms.openlocfilehash: 59df226e2740dbda3a67e0c3c49d688a3e564fee
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50622861"
---
# <a name="compiler-error-c2875"></a>컴파일러 오류 C2875

using 선언 하면 'class::identifier'의 여러 선언

선언 하면 동일한 항목을 두 번 정의 됩니다.

다음 샘플에서는 C2875 오류가 생성 됩니다.

```
// C2875.cpp
struct A {
   void f(int*);
};

struct B {
   void f(double*);
};

struct AB : A, B {
   using A::f;
   using A::f;   // C2875
   using B::f;
};
```