---
title: 컴파일러 오류 C2258
ms.date: 11/04/2016
f1_keywords:
- C2258
helpviewer_keywords:
- C2258
ms.assetid: 105eaa87-befb-4ecb-9a3f-e09e14d2f5bf
ms.openlocfilehash: 99936026929bbaad321abfaa106df41b99c5d19d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50587800"
---
# <a name="compiler-error-c2258"></a>컴파일러 오류 C2258

순수 구문이 잘못되었습니다. '= 0'이어야 합니다.

순수 가상 함수를 잘못된 구문으로 선언했습니다.

다음 샘플에서는 C2258을 생성합니다.

```
// C2258.cpp
// compile with: /c
class A {
public:
   void virtual func1() = 1; // C2258
   void virtual func2() = 0;   // OK
};
```