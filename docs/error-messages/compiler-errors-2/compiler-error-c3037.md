---
title: 컴파일러 오류 C3037 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3037
dev_langs:
- C++
helpviewer_keywords:
- C3037
ms.assetid: 9ba8a890-d3c7-4cce-93c5-d358e2bfad28
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a3846aec8810e04813122a9c95c823fa99b3d698
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46089296"
---
# <a name="compiler-error-c3037"></a>컴파일러 오류 C3037

'var': 'reduction' 절의 변수는 바깥쪽 컨텍스트에서 shared여야 합니다.

[reduction](../../parallel/openmp/reference/reduction.md) 절에 지정된 변수는 컨텍스트의 각 스레드에 private일 수 없습니다.

다음 샘플에서는 C3037을 생성합니다.

```
// C3037.cpp
// compile with: /openmp /c
int g_i;

int main() {
   int i;

   #pragma omp parallel private(g_i)
   // try the following line instead
   // #pragma omp parallel
   {
      #pragma omp for reduction(+:g_i)   // C3037
      for (i = 0 ; i < 10 ; ++i) {
         g_i += i;
      }
   }
}
```