---
title: 컴파일러 오류 C2276
ms.date: 11/04/2016
f1_keywords:
- C2276
helpviewer_keywords:
- C2276
ms.assetid: 62005ad9-6cb9-4b1f-965d-b875adaf695e
ms.openlocfilehash: 2128be2be4f0b5be37bbfc5098a35bb39afe5906
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50633664"
---
# <a name="compiler-error-c2276"></a>컴파일러 오류 C2276

'operator': 바인딩된 멤버 함수 식의 연산이 잘못 되었습니다

컴파일러는 포인터 멤버를 만드는 구문 사용 하 여 문제를 발견 합니다.

다음 샘플에서는 C2276 오류가 생성 됩니다.

```
// C2276.cpp
class A {
public:
   int func(){return 0;}
} a;

int (*pf)() = &a.func;   // C2276
// try the following line instead
// int (A::*pf3)() = &A::func;

class B {
public:
   void mf() {
      &this -> mf;   // C2276
      // try the following line instead
      // &B::mf;
   }
};

int main() {
   A a;
   &a.func;   // C2276
   // try the following line instead
   // &A::func;
}
```