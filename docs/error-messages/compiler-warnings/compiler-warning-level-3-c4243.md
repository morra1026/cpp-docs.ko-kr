---
title: 컴파일러 경고 (수준 3) C4243 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4243
dev_langs:
- C++
helpviewer_keywords:
- C4243
ms.assetid: ca72f9ad-ce0b-43a9-a68c-106e1f8b90ef
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b407939b58d1025698f7c3d82bbe1921b33f90a5
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46025687"
---
# <a name="compiler-warning-level-3-c4243"></a>컴파일러 경고(수준 3) C4243

'conversion type' 변환이 'type1'에서 'type2'에 있지만 액세스할 수 없는

파생된 클래스에 대 한 포인터를 기본 클래스에 대 한 포인터로 변환 됩니다 있지만 파생된 클래스는 private 또는 protected 액세스를 사용 하 여 기본 클래스를 상속 합니다.

다음 샘플에서는 C4243 오류가 생성 됩니다.

```
// C4243.cpp
// compile with: /W3
// C4243 expected
struct B {
   int f() {
      return 0;
   };
};

struct D : private B {};
struct E : public B {};

int main() {
   // Delete the following 2 lines to resolve.
   int (D::* d)() = (int(D::*)()) &B::f;
   d;

   int (E::* e)() = (int(E::*)()) &B::f; // OK
   e;
}
```