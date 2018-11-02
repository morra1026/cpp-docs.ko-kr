---
title: 컴파일러 오류 C2460
ms.date: 11/04/2016
f1_keywords:
- C2460
helpviewer_keywords:
- C2460
ms.assetid: d969fca9-3ac5-4e4e-88fc-df05510e2093
ms.openlocfilehash: 414b6e53cf1610a55db984a1127bfc884102494f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50589594"
---
# <a name="compiler-error-c2460"></a>컴파일러 오류 C2460

'identifier1': 사용 하 여 'identifier2'에 정의 되는

클래스 또는 구조체 (`identifier2`)을 멤버 자체로로 선언 됩니다 (`identifier1`). 클래스 및 구조체의 재귀 정의 허용 되지 않습니다.

다음 샘플에서는 C2460 오류가 생성 됩니다.

```
// C2460.cpp
class C {
   C aC;    // C2460
};
```

대신, 클래스에 대 한 포인터 참조를 사용 합니다.

```
// C2460.cpp
class C {
   C * aC;    // OK
};
```