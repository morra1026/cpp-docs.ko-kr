---
title: 컴파일러 오류 C2876
ms.date: 11/04/2016
f1_keywords:
- C2876
helpviewer_keywords:
- C2876
ms.assetid: 8b674bf1-f9f4-4a8e-8127-e884c1d1708f
ms.openlocfilehash: e7fcdeaf79728ee99498c69de0205619d16612d8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50664726"
---
# <a name="compiler-error-c2876"></a>컴파일러 오류 C2876

'class::symbol': 액세스할 수 있는 일부 오버 로드

기본 클래스에서 함수의 모든 오버 로드 된 폼 파생된 클래스에 액세스할 수 있어야 합니다.

다음 샘플에서는 C2876 오류가 생성 됩니다.

```
// C2876.cpp
// compile with: /c
class A {
public:
   double a(double);
private:
   int a(int);
};

class B : public A {
   using A::a;   // C2876 one overload is private in base class
};
```