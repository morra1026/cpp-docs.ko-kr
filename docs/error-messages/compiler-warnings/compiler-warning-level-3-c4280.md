---
title: 컴파일러 경고(수준 3) C4280
ms.date: 11/04/2016
f1_keywords:
- C4280
helpviewer_keywords:
- C4280
ms.assetid: 153fb639-3ee1-4fee-baf9-71420abcf3f6
ms.openlocfilehash: 6a3daa9903cbf983ddc19538a154d9717a2f9f0f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50618935"
---
# <a name="compiler-warning-level-3-c4280"></a>컴파일러 경고(수준 3) C4280

'type' 형식을 통해 재귀적을 된 'operator->'

코드 잘못 사용 **operator->** 자신을 호출 합니다.

다음 샘플에서는 C4280 오류가 생성 됩니다.

```
// C4280.cpp
// compile with: /W3 /WX
struct A
{
   int z;
   A& operator ->();
};

void f(A y)
{
   int i = y->z; // C4280
}
```