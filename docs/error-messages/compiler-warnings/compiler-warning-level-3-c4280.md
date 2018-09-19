---
title: 컴파일러 경고 (수준 3) C4280 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4280
dev_langs:
- C++
helpviewer_keywords:
- C4280
ms.assetid: 153fb639-3ee1-4fee-baf9-71420abcf3f6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: aa1446e6725ecbb990e38ede33071afddb54065f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46118325"
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