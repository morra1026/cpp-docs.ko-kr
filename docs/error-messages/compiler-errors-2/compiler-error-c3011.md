---
title: 컴파일러 오류 C3011 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3011
dev_langs:
- C++
helpviewer_keywords:
- C3011
ms.assetid: 24c3a917-ebff-4deb-9155-23adf6468531
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3f25e3f9479b2555badbd079c3e2d939e91acbba
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46024413"
---
# <a name="compiler-error-c3011"></a>컴파일러 오류 C3011

병렬 영역 내부에서는 직접 인라인 어셈블리를 사용할 수 없습니다.

`omp` 병렬 영역은 인라인 어셈블리 명령을 포함할 수 없습니다.

다음 샘플에서는 C3011을 생성합니다.

```
// C3011.cpp
// compile with: /openmp
// processor: /x86
int main() {
   int   n = 0;

   #pragma omp parallel
   {
      _asm mov eax, n   // Delete this line to resolve this error.
   }   // C3011
}
```