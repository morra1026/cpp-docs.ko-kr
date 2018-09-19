---
title: 컴파일러 오류 C2819 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2819
dev_langs:
- C++
helpviewer_keywords:
- C2819
ms.assetid: fcc7762d-cb82-4bb1-a715-0d82da832edf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e535b47828a70a7a2e52606bc5c9de6ceb62ee48
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46095449"
---
# <a name="compiler-error-c2819"></a>컴파일러 오류 C2819

'type' 형식에 오버로드된 멤버 'operator ->'가 없습니다.

정의 해야 `operator->()` 이 포인터 연산을 사용 하도록 합니다.

다음 샘플에서는 C2819 오류가 생성 됩니다.

```
// C2819.cpp
// compile with: /c
class A {
   public:
      int i;
};

class B {};

void C(B j) {
   j->i;   // C2819
}

class D {
   A* pA;

   public:
      A* operator->() {
         return pA;
      }
};

void F(D j) {
   j->i;
}
```

사용 하는 경우에 C2819 발생할 수 있습니다 [참조 형식에 대 한 c + + 스택 의미 체계](../../dotnet/cpp-stack-semantics-for-reference-types.md)합니다. 다음 샘플에서는 C2819 오류가 생성 됩니다.

```
// C2819_b.cpp
// compile with: /clr
ref struct R {
   void Test() {}
};

int main() {
   R r;
   r->Test();   // C2819
   r.Test();   // OK
}
```