---
title: 컴파일러 오류 C2105
ms.date: 11/04/2016
f1_keywords:
- C2105
helpviewer_keywords:
- C2105
ms.assetid: 19b7f7bc-a9da-4d23-8193-005b6d09274f
ms.openlocfilehash: d47ee2815a3ba5609fcdc6b7312ac8c6187ec861
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50631766"
---
# <a name="compiler-error-c2105"></a>컴파일러 오류 C2105

'연산자'에 l-value가 필요합니다.

피연산자와 연산자에는 l-value가 있어야 합니다.

다음 샘플에서는 C2105를 생성합니다.

```
// C2105.cpp
int main() {
   unsigned char * p1 = 0;
   unsigned int * p2 = (unsigned int *)p1;
   p2++;

   unsigned int * p = 0;
   p++;   // ok

   p2 = (unsigned int *)p1;
   ((unsigned int *)p1)++;   // C2105
}
```

다음 샘플에서는 C2105를 생성합니다.

```
// C2105b.cpp
int main() {
   int a[10] = {0};
   int b[10] = {0};
   ++(a , b);   // C2105

   // OK
   ++(a[0] , b[0]);
   ++a[0];
}
```