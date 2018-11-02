---
title: 컴파일러 오류 C2689
ms.date: 11/04/2016
f1_keywords:
- C2689
helpviewer_keywords:
- C2689
ms.assetid: b5216fba-524d-4194-9168-26e9dc5210ce
ms.openlocfilehash: fb9a45f775da582daa0fbe421f29b6e469a91197
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50484554"
---
# <a name="compiler-error-c2689"></a>컴파일러 오류 C2689

'function': 지역 클래스 내에서 friend 함수를 정의할 수 없습니다

선언할 수 있지만 로컬 클래스의 friend 함수를 정의 하지 않습니다.

다음 샘플에서는 C2689 오류가 생성 됩니다.

```
// C2689.cpp
// compile with: /c
void g() {
   void f2();
   class X {
      friend void f2(){}   // C2689
      friend void f2();   // OK
   };
}
```