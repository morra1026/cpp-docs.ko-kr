---
title: 컴파일러 오류 C3009
ms.date: 11/04/2016
f1_keywords:
- C3009
helpviewer_keywords:
- C3009
ms.assetid: aded5985-f5fd-4c3e-a157-16be55ec1313
ms.openlocfilehash: a1f4a20396e97c6b868a5678958970813b638499
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50597199"
---
# <a name="compiler-error-c3009"></a>컴파일러 오류 C3009

'label': OpenMP 구조화된 블록 외부에서 내부로 점프할 수 없습니다.

코드가 OpenMP 블록 안이나 밖으로 점프할 수 없습니다.

다음 샘플에서는 C3009를 생성합니다.

```
// C3009.c
// compile with: /openmp
int main() {
   #pragma omp parallel
   {
   lbl2:;
   }
   goto lbl2;   // C3009
}
```