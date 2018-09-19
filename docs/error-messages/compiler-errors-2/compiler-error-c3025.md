---
title: 컴파일러 오류 C3025 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3025
dev_langs:
- C++
helpviewer_keywords:
- C3025
ms.assetid: 4442f5a3-d9ea-4873-b1fb-e7e5bd3cbe5e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2b96737e788134f70ec203ca9f0cb67c99e0628c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46115062"
---
# <a name="compiler-error-c3025"></a>컴파일러 오류 C3025

'clause': 정수 계열 식이 있어야 합니다.

절에 정수 식이 필요하지만 정수가 아닌 식이 제공되었습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3025를 생성합니다.

```
// C3025.cpp
// compile with: /openmp /link vcomps.lib
#include <stdio.h>
#include "omp.h"

float f = 2.0F;

int main()
{
    int i = 0;

    // OK
    puts("Test with int");
    #pragma omp parallel for num_threads(i)
    for (i = 1; i <= 2; ++i)
        printf_s("Hello World - thread %d - iteration %d\n",
                 omp_get_thread_num(), i);

    puts("Test with float");
    #pragma omp parallel for num_threads(f)   // C3025
    for (i = 1; i <= 2; ++i)
        printf_s("Hello World - thread %d - iteration %d\n",
                 omp_get_thread_num(), i);
}
```