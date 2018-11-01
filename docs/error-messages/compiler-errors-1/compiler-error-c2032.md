---
title: 컴파일러 오류 C2032
ms.date: 11/04/2016
f1_keywords:
- C2032
helpviewer_keywords:
- C2032
ms.assetid: 625d7c83-70b6-42c2-a558-81fbc0026324
ms.openlocfilehash: 5743aba880f23d7706940936fc4a3a1973a84ca1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50558251"
---
# <a name="compiler-error-c2032"></a>컴파일러 오류 C2032

'identifier': 함수는 'structorunion' 구조체/공용 구조체의 멤버일 수 없습니다

구조체 또는 공용 구조체에 3. 아니라 c + +에서 허용 되는 멤버 함수 오류를 해결 하려면 c + + 프로그램 컴파일 또는 멤버 함수를 제거 합니다.

다음 샘플에서는 C2032 오류가 생성 됩니다.

```
// C2032.c
struct z {
   int i;
   void func();   // C2032
};
```

해결 방법:

```
// C2032b.c
// compile with: /c
struct z {
   int i;
};
```