---
title: 컴파일러 오류 C2883 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2883
dev_langs:
- C++
helpviewer_keywords:
- C2883
ms.assetid: 5c6d689d-ed42-41ad-b5c0-e9c2e0b8c356
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 50cc5b2abb34fae21bea78aa146e74b9aa9491c4
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46019265"
---
# <a name="compiler-error-c2883"></a>컴파일러 오류 C2883

'name': 함수 선언이 using 선언에 의해 도입 된 'identifier'를 사용 하 여 충돌

함수를 두 번 이상 정의 하려고 했습니다. 첫 번째 정의 네임 스페이스가에서 수행 된 `using` 선언 합니다. 두 번째 지역 정의 했습니다.

다음 샘플에서는 C2883 오류가 생성 됩니다.

```
// C2883.cpp
namespace A {
   void z(int);
}

int main() {
   using A::z;
   void z(int);   // C2883  z is already defined
}
```