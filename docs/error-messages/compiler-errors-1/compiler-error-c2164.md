---
title: 컴파일러 오류 C2164
ms.date: 11/04/2016
f1_keywords:
- C2164
helpviewer_keywords:
- C2164
ms.assetid: 55df5024-68a8-45a8-ae6c-e6dba35318a2
ms.openlocfilehash: 3b1c7a94dfca1c2767e14f96204ecda670c8a586
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50460816"
---
# <a name="compiler-error-c2164"></a>컴파일러 오류 C2164

'function': 내장 함수를 선언 하지

`intrinsic` 가 선언 되지 않은 함수를 사용 하는 pragma (에서만 발생 **/Oi**). 또는 해당 헤더 파일을 포함 하지 않고 컴파일러 내장 함수 중 하나를 사용 했습니다.

다음 샘플에서는 C2164 오류가 생성 됩니다.

```
// C2164.c
// compile with: /c
// processor: x86
// Uncomment the following line to resolve.
// #include "xmmintrin.h"
void b(float *p) {
   _mm_load_ss(p);   // C2164
}
```