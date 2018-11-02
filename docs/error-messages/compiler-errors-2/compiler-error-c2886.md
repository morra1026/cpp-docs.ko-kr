---
title: 컴파일러 오류 C2886
ms.date: 11/04/2016
f1_keywords:
- C2886
helpviewer_keywords:
- C2886
ms.assetid: c01588a1-484c-4dc9-a3f1-f900c6e44543
ms.openlocfilehash: 2fa7450f03505501c2c4a45023dbb6a86937bb9c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50586682"
---
# <a name="compiler-error-c2886"></a>컴파일러 오류 C2886

'class::identifier': 멤버 using 선언에서 기호를 사용할 수 없습니다

`using` 선언 네임 스페이스 이름과 같은 기호를 사용 합니다. `using` 선언이 기본 클래스 멤버를 선언 합니다.

다음 샘플에서는 C2886 오류가 생성 됩니다.

```
// C2886.cpp
// compile with: /c
namespace Z {
    int i;
}

class B {
protected:
    int i;
};

class D : public B {
    // Error: Z is a namespace
    using Z::i;   // C2886

    // OK: B is a base class
    using B::i;
};
```