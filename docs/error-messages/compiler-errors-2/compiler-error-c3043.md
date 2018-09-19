---
title: 컴파일러 오류 C3043 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3043
dev_langs:
- C++
helpviewer_keywords:
- C3043
ms.assetid: 0ef55e63-e82b-48eb-9d44-690950ac34c6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ff64629e5385185f524a4f76d9b959d107b53563
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46041716"
---
# <a name="compiler-error-c3043"></a>컴파일러 오류 C3043

OpenMP 'critical' 지시문은 같은 이름의 'critical' 지시문 내부에 중첩될 수 없습니다.

[critical](../../parallel/openmp/reference/critical.md) 지시문은 같은 이름을 사용하는 `critical` 지시문 내부에 중첩될 수 없습니다.

다음 샘플에서는 C3043을 생성합니다.

```
// C3043.cpp
// compile with: /openmp /c
#include "omp.h"

int main() {
   int n1 = 1, n2 = 2, n3 = 3;

   #pragma omp parallel
   {
      ++n2;

      #pragma omp critical(MyTest)
      {
         ++n2;

         #pragma omp critical(MyTest)   // C3043
         // try the following line instead
         // #pragma omp critical(MyTest2)
         {
            ++n3;
         }
      }
   }
}
```