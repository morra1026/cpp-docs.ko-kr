---
title: 컴파일러 오류 C3055 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3055
dev_langs:
- C++
helpviewer_keywords:
- C3055
ms.assetid: 60446ee0-18dd-48fc-9059-f0a14229dce8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6fa27d9c6230c2cdebae4f718904ddd7cc1a7208
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46111084"
---
# <a name="compiler-error-c3055"></a>컴파일러 오류 C3055

'symbol': 'threadprivate' 지시문에 사용된 기호만 참조할 수 있습니다.

기호가 참조된 다음 [threadprivate](../../parallel/openmp/reference/threadprivate.md) 절에서 사용되며 이는 허용되지 않습니다.

다음 샘플에서는 C3055를 생성합니다.

```
// C3055.cpp
// compile with: /openmp
int x, y;
int z = x;
#pragma omp threadprivate(x, y)   // C3055

void test() {
   #pragma omp parallel copyin(x, y)
   {
      x = y;
   }
}
```

해결 방법:

```
// C3055b.cpp
// compile with: /openmp /LD
int x, y, z;
#pragma omp threadprivate(x, y)

void test() {
   #pragma omp parallel copyin(x, y)
   {
      x = y;
   }
}
```