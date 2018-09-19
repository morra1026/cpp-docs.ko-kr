---
title: 컴파일러 오류 C3033 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3033
dev_langs:
- C++
helpviewer_keywords:
- C3033
ms.assetid: 8628b6bb-a650-4ed2-af13-57acd2f7ddbb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 61e1b1c4a5711b18263f22ce8344beb383eeafdb
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46051804"
---
# <a name="compiler-error-c3033"></a>컴파일러 오류 C3033

'var': 'clause' 절의 변수는 const 한정 형식이 될 수 없습니다.

특정 절에 전달된 값은 `const` 변수가 될 수 없습니다.

다음 샘플에서는 C3033을 생성합니다.

```
// C3033.cpp
// compile with: /openmp /link vcomps.lib
int main() {
   const int val = 1;
   int val2 = 1;

   #pragma omp parallel reduction(+ : val)   // C3033
   ;

   #pragma omp parallel reduction(+ : val2)   // OK
   ;
}
```