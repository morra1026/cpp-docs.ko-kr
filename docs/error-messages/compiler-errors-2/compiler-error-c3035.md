---
title: 컴파일러 오류 C3035 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3035
dev_langs:
- C++
helpviewer_keywords:
- C3035
ms.assetid: af34fad2-2b45-42d0-a9ff-04eab3e91c37
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1e3be9974d299018af77bde0989b1bdc18889706
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46081574"
---
# <a name="compiler-error-c3035"></a>컴파일러 오류 C3035

OpenMP 'ordered' 지시문은 'ordered' 절이 있는 'for' 또는 'parallel for' 지시문에 직접 바인딩되어야 합니다.

순서가 지정된 절의 형식이 잘못되었습니다.

다음 샘플에서는 C3035를 생성합니다.

```
// C3035.cpp
// compile with: /openmp /link vcomps.lib
int main() {
   int n = 0, x, i;

   #pragma omp parallel private(n)
   {
      #pragma omp ordered   // C3035
      // Try the following line instead:
      // #pragma omp for ordered
       for (i = 0 ; i < 10 ; ++i)
         ;
   }
}
```