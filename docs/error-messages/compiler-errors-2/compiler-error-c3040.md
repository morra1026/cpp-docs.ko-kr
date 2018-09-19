---
title: 컴파일러 오류 C3040 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3040
dev_langs:
- C++
helpviewer_keywords:
- C3040
ms.assetid: 29e857ac-74f0-4ec6-becf-9026e38c160e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 419178a7ff71817c418aa791ae1f6cce116cd986
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46057695"
---
# <a name="compiler-error-c3040"></a>컴파일러 오류 C3040

'var': 'reduction' 절의 변수 형식이 환산 연산자 'operator'와 호환되지 않습니다.

[reduction](../../parallel/openmp/reference/reduction.md) 절의 변수를 reduction 연산자와 함께 사용할 수 없습니다.

다음 샘플에서는 C3040을 생성합니다.

```
// C3040.cpp
// compile with: /openmp /c
#include "omp.h"
double d;

int main() {
   #pragma omp parallel reduction(&:d)   // C3040
      ;

   #pragma omp parallel reduction(-:d)  // OK
      ;
}
```