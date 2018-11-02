---
title: 컴파일러 오류 C3053
ms.date: 11/04/2016
f1_keywords:
- C3053
helpviewer_keywords:
- C3053
ms.assetid: ab9a25f3-e341-4f6e-8e69-069b4a963a64
ms.openlocfilehash: cb01207be15a628fb0c6206df3e6a673067f568a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50441371"
---
# <a name="compiler-error-c3053"></a>컴파일러 오류 C3053

'symbol': 'threadprivate'는 글로벌 또는 정적 데이터 항목에만 사용할 수 있습니다.

[threadprivate](../../parallel/openmp/reference/threadprivate.md) 에 전달된 기호는 전역 또는 정적이어야 합니다.

다음 샘플에서는 C3053을 생성합니다.

```
// C3053.cpp
// compile with: /openmp
void Test() {
   int x, y;
   #pragma omp threadprivate(x, y)   // C3053
   #pragma omp parallel copyin(x, y)
   {
      x = y;
   }
}
```

해결 방법:

```
// C3053b.cpp
// compile with: /openmp /LD
int x, y;
#pragma omp threadprivate(x, y)

void Test() {
   #pragma omp parallel copyin(x, y)
   {
      x = y;
   }
}
```