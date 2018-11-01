---
title: 컴파일러 오류 C2034
ms.date: 11/04/2016
f1_keywords:
- C2034
helpviewer_keywords:
- C2034
ms.assetid: 953d70fa-bde9-4ce6-a55d-741e7bc63ff4
ms.openlocfilehash: 4b4fe769f78e5f826ba08d4819019210f21f860f
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50479679"
---
# <a name="compiler-error-c2034"></a>컴파일러 오류 C2034

'identifier': 비트 수가 너무 작아서 비트 필드의 형식

비트 필드 선언에는 비트 수가 기본 형식의 크기를 초과합니다.

다음 샘플에서는 C2034를 생성합니다.

```
// C2034.cpp
struct A {
   char test : 9;   // C2034, char has 8 bits
};
```

해결 방법:

```
// C2034b.cpp
// compile with: /c
struct A {
   char test : 8;
};
```