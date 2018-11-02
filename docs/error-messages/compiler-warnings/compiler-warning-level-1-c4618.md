---
title: 컴파일러 경고(수준 1) C4618
ms.date: 11/04/2016
f1_keywords:
- C4618
helpviewer_keywords:
- C4618
ms.assetid: 6ff10d0a-6d5b-4373-8196-1d57bb6b1611
ms.openlocfilehash: b8f24df7465525b24ecd3871447bd873889b1e23
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50583805"
---
# <a name="compiler-warning-level-1-c4618"></a>컴파일러 경고(수준 1) C4618

pragma 매개 변수는 빈 문자열을 포함 pragma가 무시 됩니다

인수로 지정 된 null 문자열을 **#pragma**합니다.

Pragma는 인수 없이 처리 됩니다.

다음 샘플에서는 C4618 오류가 생성 됩니다.

```
// C4618.cpp
// compile with: /W1 /LD
#pragma code_seg("")   // C4618
```