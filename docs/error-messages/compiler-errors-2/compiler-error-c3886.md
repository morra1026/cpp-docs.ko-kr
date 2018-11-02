---
title: 컴파일러 오류 C3886
ms.date: 11/04/2016
f1_keywords:
- C3886
helpviewer_keywords:
- C3886
ms.assetid: 485f6c12-cc1b-4146-9034-409a0a5e615e
ms.openlocfilehash: 68ed8d6cf208ae2a53e196e7b430eae1f8fe3ca0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50471801"
---
# <a name="compiler-error-c3886"></a>컴파일러 오류 C3886

'var': 리터럴 데이터 멤버를 초기화 합니다

A [리터럴](../../windows/literal-cpp-component-extensions.md) 변수를 선언할 때 초기화 해야 합니다.

다음 샘플에서는 C3886를 생성합니다.

```
// C3886.cpp
// compile with: /clr /c
ref struct Y1 {
   literal int staticConst;   // C3886
   literal int staticConst2 = 0;   // OK
};
```