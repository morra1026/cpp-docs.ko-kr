---
title: 컴파일러 오류 C3024 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3024
dev_langs:
- C++
helpviewer_keywords:
- C3024
ms.assetid: 1c031c28-ce37-4de3-aead-cfe76b261856
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 85d087fc31b0eed2f6b4a35d89b20b6fd016cc9b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46078662"
---
# <a name="compiler-error-c3024"></a>컴파일러 오류 C3024

'schedule(runtime)' : chunk_size 식은 허용되지 않습니다.

schedule 절의 런타임 매개 변수에 값을 전달할 수 없습니다.

다음 샘플에서는 C3024를 생성합니다.

```
// C3024.cpp
// compile with: /openmp /link vcomps.lib
#include <stdio.h>
#include "omp.h"

int main() {
   int i;

   #pragma omp parallel for schedule(runtime, 10)   // C3024
   for (i = 0; i < 10; ++i) ;

   #pragma omp parallel for schedule(runtime)   // OK
   for (i = 0; i < 10; ++i) ;
}
```