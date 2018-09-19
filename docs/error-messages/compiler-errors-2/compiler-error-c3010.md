---
title: 컴파일러 오류 C3010 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3010
dev_langs:
- C++
helpviewer_keywords:
- C3010
ms.assetid: e959d038-bba6-432a-9c0a-0470474de7d9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d68be11a510ba41197cb9645484a10ca8dae6d77
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46075126"
---
# <a name="compiler-error-c3010"></a>컴파일러 오류 C3010

'label': OpenMP 구조화된 블록 내부에서 외부로 점프할 수 없습니다.

코드가 OpenMP 블록 안이나 밖으로 점프할 수 없습니다.

다음 샘플에서는 C3010을 생성합니다.

```
// C3010.c
// compile with: /openmp
int main() {
   #pragma omp parallel
   {
      #pragma omp parallel
      {
         goto lbl3;
      }
   }
   lbl3:;   // C3010
}
```