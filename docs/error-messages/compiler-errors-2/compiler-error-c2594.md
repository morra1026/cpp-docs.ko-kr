---
title: 컴파일러 오류 C2594 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2594
dev_langs:
- C++
helpviewer_keywords:
- C2594
ms.assetid: 68cd708f-266e-44b0-a211-3e3ab63b11bf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9be22544930bb94c36ec5906cbf60d5caac143fe
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46058018"
---
# <a name="compiler-error-c2594"></a>컴파일러 오류 C2594

'operator': 'type1'에서 'type2'의 모호한 변환입니다.

변환이 *type1* 하 *type2* 다른 보다 직접적 합니다. 변환 하기 위한 두 가지 방법이 것이 좋습니다 *type1* 하 *type2*합니다. 첫 번째 옵션에서 직접 변환을 정의 하는 것 *type1* 하 *type2*를 두 번째 옵션에서 변환의 순서를 지정 하 고 *type1* 를  *type2*합니다.

다음 샘플 C2594를 생성합니다. 오류에 대 한 권장된 해결 방법의 변환 순서 같습니다.

```
// C2594.cpp
// compile with: /c
struct A{};
struct I1 : A {};
struct I2 : A {};
struct D : I1, I2 {};

A *f (D *p) {
   return (A*) (p);    // C2594

// try the following line instead
// return static_cast<A *>(static_cast<I1 *>(p));
}
```