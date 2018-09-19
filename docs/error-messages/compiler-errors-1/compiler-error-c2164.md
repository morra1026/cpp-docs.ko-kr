---
title: 컴파일러 오류 C2164 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2164
dev_langs:
- C++
helpviewer_keywords:
- C2164
ms.assetid: 55df5024-68a8-45a8-ae6c-e6dba35318a2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b1e997a3b260b9ec8b68a92967233269707e6888
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46032161"
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