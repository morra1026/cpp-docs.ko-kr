---
title: 컴파일러 오류 C2638
ms.date: 11/04/2016
f1_keywords:
- C2638
helpviewer_keywords:
- C2638
ms.assetid: 9d4275e8-406d-455e-afee-3a37799230e0
ms.openlocfilehash: 0c4c1e73c97f51bb0e52a618829ffb0bed417a45
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50582779"
---
# <a name="compiler-error-c2638"></a>컴파일러 오류 C2638

'identifier': __based 한정자를 멤버에 대 한 포인터

`__based` 멤버에 대 한 포인터에 대 한 한정자를 사용할 수 없습니다.

다음 샘플에서는 C2638 오류가 생성 됩니다.

```
// C2638.cpp
void *a;

class C {
public:
   int i;
   int j;
   int func();
};
int __based (a) C::* cpi = &C::i;  // C2638
int (__based (a) C::* cpf)() = &C::func; // c2638
```