---
title: 컴파일러 오류 C3010
ms.date: 11/04/2016
f1_keywords:
- C3010
helpviewer_keywords:
- C3010
ms.assetid: e959d038-bba6-432a-9c0a-0470474de7d9
ms.openlocfilehash: c5f0d33632cb155b8365c8de421fa5eaf91421c6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50455499"
---
# <a name="compiler-error-c3010"></a>컴파일러 오류 C3010

'label': OpenMP 구조화된 블록 내부에서 외부로 점프할 수 없습니다.

코드가 OpenMP 블록 안이나 밖으로 점프할 수 없습니다.

다음 샘플에서는 C3010을 생성합니다.

```
// C3010.c
// compile with: /openmp
int main() {
   #pragma omp parallel
   {
      #pragma omp parallel
      {
         goto lbl3;
      }
   }
   lbl3:;   // C3010
}
```