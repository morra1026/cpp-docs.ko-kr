---
title: 컴파일러 경고(수준 1) C4224
ms.date: 11/04/2016
f1_keywords:
- C4224
helpviewer_keywords:
- C4224
ms.assetid: 1531cae0-5040-49fd-b149-005bb5085391
ms.openlocfilehash: ed27e6ff63e3d5f3bab4f6d8d9639b84a5606ff2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50563942"
---
# <a name="compiler-warning-level-1-c4224"></a>컴파일러 경고(수준 1) C4224

비표준 확장이 사용 됨: 'identifier' 정식 매개 변수 형식으로 이전에 정의한

식별자로 이전에 사용한를 `typedef`입니다. 이렇게 하면 경고 ANSI 호환성 ([/Za](../../build/reference/za-ze-disable-language-extensions.md)).

## <a name="example"></a>예제

```
// C4224.cpp
// compile with: /Za /W1 /LD
typedef int I;
void func ( int I );  // C4224
```