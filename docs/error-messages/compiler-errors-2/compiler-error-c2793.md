---
title: 컴파일러 오류 C2793
ms.date: 11/04/2016
f1_keywords:
- C2793
helpviewer_keywords:
- C2793
ms.assetid: ce35f4e8-c357-40ca-95c4-15ff001ad69d
ms.openlocfilehash: 5533a0e8f75a1a513fbabe451fb41629a4595382
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50428186"
---
# <a name="compiler-error-c2793"></a>컴파일러 오류 C2793

'token': 예기치 않은 토큰 다음 ': ', 식별자 또는 키워드 'operator'가 필요 합니다.

수행할 수 있는 토큰 `__super::` 식별자 또는 키워드 `operator`합니다.

다음 샘플에서는 C2793

```
// C2793.cpp
struct B {
   void mf();
};

struct D : B {
   void mf() {
      __super::(); // C2793
   }
};
```