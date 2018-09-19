---
title: 컴파일러 오류 C2319 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2319
dev_langs:
- C++
helpviewer_keywords:
- C2319
ms.assetid: 25263e6e-f5ba-4d2c-8727-8c2d8ca2e5ce
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f485d26ac2a05cc91a1c918c63e319e893b8cf95
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46103154"
---
# <a name="compiler-error-c2319"></a>컴파일러 오류 C2319

'try/catch'는 복합 문이 뒤에 와야 합니다. '{'가 없습니다.

`try` 또는 `catch` 블록이 `try` 또는 `catch` 문 다음에 오지 않습니다. 블록은 중괄호로 묶어야 합니다.

다음 샘플에서는 C2319를 생성합니다.

```
// C2319.cpp
// compile with: /EHsc
#include <eh.h>
class C {};
int main() {
   try {
      throw "ooops!";
   }
   catch( C ) ;    // C2319
   // try the following line instead
   // catch( C ) {}
}
```