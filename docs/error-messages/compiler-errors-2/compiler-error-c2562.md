---
title: 컴파일러 오류 C2562
ms.date: 11/04/2016
f1_keywords:
- C2562
helpviewer_keywords:
- C2562
ms.assetid: 2c41e511-9952-4b98-9976-6b1523613e1b
ms.openlocfilehash: c665c4ed82fefaf0ee724defb8c205f86fc06dd0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50435311"
---
# <a name="compiler-error-c2562"></a>컴파일러 오류 C2562

'identifier': 'void' 함수는 값을 반환

으로 선언 `void` 되었지만 값을 반환 합니다.

이 오류는 잘못 된 함수 프로토타입에서 발생할 수 있습니다.

반환 형식이 함수 선언에서 지정 하면이 오류를 해결할 수 있습니다.

다음 샘플에서는 C2562 오류가 생성 됩니다.

```
// C2562.cpp
// compile with: /c
void testfunc() {
   int i;
   return i;   // C2562 delete the return to resolve
}
```