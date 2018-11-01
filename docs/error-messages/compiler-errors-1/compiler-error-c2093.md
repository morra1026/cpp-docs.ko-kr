---
title: 컴파일러 오류 C2093
ms.date: 11/04/2016
f1_keywords:
- C2093
helpviewer_keywords:
- C2093
ms.assetid: 17529a70-9169-46b5-9fc6-57a5ce224e6a
ms.openlocfilehash: d57b452e63f7bf76051ef6a23c5f8f6ba81aed1e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50511152"
---
# <a name="compiler-error-c2093"></a>컴파일러 오류 C2093

'variable1': '변수 2' 자동 변수의 주소를 사용 하 여 초기화할 수 없습니다.

사용 하 여 컴파일하면 [/Za](../../build/reference/za-ze-disable-language-extensions.md), 프로그램 이니셜라이저로 자동 변수의 주소를 사용 하려고 합니다.

다음 샘플에서는 C2093 오류가 생성 됩니다.

```
// C2093.c
// compile with: /Za /c
void func() {
   int li;   // an implicit auto variable
   int * s[]= { &li };   // C2093 address is not a constant

   // OK
   static int li2;
   int * s2[]= { &li2 };
}
```