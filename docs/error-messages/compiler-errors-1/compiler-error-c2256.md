---
title: 컴파일러 오류 C2256
ms.date: 11/04/2016
f1_keywords:
- C2256
helpviewer_keywords:
- C2256
ms.assetid: 171fa2bc-8c72-49cd-afe5-d723b7acd3c5
ms.openlocfilehash: 56c4df338feb2c0f406835c1ef2ffeeb7caf8bca
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50582708"
---
# <a name="compiler-error-c2256"></a>컴파일러 오류 C2256

'function'에서 friend 지정자를 잘못 사용 했습니다.

소멸자 또는 생성자로 지정할 수 없습니다는 [friend](../../cpp/friend-cpp.md)합니다.

다음 샘플에서는 C2256 오류가 생성 됩니다.

```
// C2256.cpp
// compile with: /c
class C {
public:
   friend ~C();   // C2256
   ~C();   // OK
};
```