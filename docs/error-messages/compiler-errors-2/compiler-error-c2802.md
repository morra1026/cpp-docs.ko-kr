---
title: 컴파일러 오류 C2802
ms.date: 11/04/2016
f1_keywords:
- C2802
helpviewer_keywords:
- C2802
ms.assetid: 08b68c0e-9382-40ac-8949-39a7a2749e05
ms.openlocfilehash: 9024a13b0e4fdbc4174f94e6c0c8736b03f3c221
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50538738"
---
# <a name="compiler-error-c2802"></a>컴파일러 오류 C2802

정적 멤버 'operator o'에 정식 매개 변수가 없음

선언한 연산자는 `static` 멤버 함수는 매개 변수가 하나 이상 있어야 합니다.

다음 샘플에서는 C2802 오류가 생성 됩니다.

```
// C2802.cpp
// compile with: /clr /c
ref class A {
   static operator+ ();   // C2802
   static operator+ (A^, A^);   // OK
};
```