---
title: 컴파일러 오류 C3736
ms.date: 11/04/2016
f1_keywords:
- C3736
helpviewer_keywords:
- C3736
ms.assetid: 579b773c-41e7-40ea-8382-2e3ce2667f4c
ms.openlocfilehash: e31d68a13ebd9c5267fd285d43ebc66ae8b53182
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50584199"
---
# <a name="compiler-error-c3736"></a>컴파일러 오류 C3736

'event': 메서드 이거나, 관리 되는 이벤트의 경우 데이터 멤버

네이티브 및 COM 이벤트에는 메서드가 있어야 합니다. .NET 이벤트 데이터 멤버를 수도 있습니다.

다음 샘플에서는 C3736 오류가 생성 됩니다.

```
// C3736.cpp
struct A {
   __event int e();
};

struct B {
   int f;   // C3736
   // The following line resolves the error.
   // int f();
   B(A* a) {
      __hook(&A::e, a, &B::f);
   }
};

int main() {
}
```