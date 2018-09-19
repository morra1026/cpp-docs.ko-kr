---
title: 컴파일러 오류 C2325 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2325
dev_langs:
- C++
helpviewer_keywords:
- C2325
ms.assetid: e6b0a186-3f2a-4adf-beae-fadd75492bf7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ae66d00c6831d102cb3f6fd47d024745480674fc
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46107814"
---
# <a name="compiler-error-c2325"></a>컴파일러 오류 C2325

'type': 'name' 오른쪽에 예기치 않은 형식

잘못 된 형식의 소멸자를 호출 합니다.

다음 샘플에서는 C2325 오류가 생성 됩니다.

```
// C2325.cpp
// compile with: /c
class A {};
typedef A* pA_t;
void f() {
    A** ppa = new A *;
    ppa->~A*;   // C2325

   pA_t *ppa2 = new pA_t;
   ppa2->~pA_t();   // OK
}
```