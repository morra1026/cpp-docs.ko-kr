---
title: 컴파일러 오류 C3015
ms.date: 11/04/2016
f1_keywords:
- C3015
helpviewer_keywords:
- C3015
ms.assetid: d5e8e50b-7542-4b2d-8665-1b22072a5bc6
ms.openlocfilehash: 97ad6b51b9444e03f17511e26be75f5a783a5f07
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50464468"
---
# <a name="compiler-error-c3015"></a>컴파일러 오류 C3015

OpenMP 'for' 문의 초기화 형식이 잘못되었습니다.

OpenMP 문의 `for` 루프를 완벽하고 명시적으로 지정해야 합니다.

다음 샘플에서는 C3015를 생성합니다.

```
// C3015.cpp
// compile with: /openmp
int main()
{
   int i = 0, j = 10;

   #pragma omp parallel
   {
      #pragma omp for
      for (; i < 0; i += j)   // C3015
      // Try the following line instead:
      // for (i = 0; i < 0; i++)
         --j;
   }
}
```