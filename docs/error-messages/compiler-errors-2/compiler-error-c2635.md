---
title: 컴파일러 오류 C2635 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2635
dev_langs:
- C++
helpviewer_keywords:
- C2635
ms.assetid: 9deca2a8-2d61-42eb-9783-6578132ee3fb
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cb7bc7b39550df7b742b2a8b940a77170e81914c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46017393"
---
# <a name="compiler-error-c2635"></a>컴파일러 오류 C2635

변환할 수 없습니다는 ' identifier1 *'는 ' identifier2\*'; 가상 기본 클래스에서 변환 인 것으로 간주

변환에서 캐스트가 필요 하지만 `virtual` 기본 클래스를 파생된 클래스는 허용 되지 않습니다.

다음 샘플에서는 C2635 오류가 생성 됩니다.

```
// C2635.cpp
class B {};
class D : virtual public B {};
class E : public B {};

int main() {
   B b;
   D d;
   E e;

   D * pD = &d;
   E * pE = &e;
   pD = (D*)&b;   // C2635
   pE = (E*)&b;   // OK
}
```