---
title: 컴파일러 오류 C2334
ms.date: 11/04/2016
f1_keywords:
- C2334
helpviewer_keywords:
- C2334
ms.assetid: 36142855-e00b-4bbf-80f5-a301edeff46e
ms.openlocfilehash: 4f068792193fd22ccddc39f9afc555e7c8672d8c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50512961"
---
# <a name="compiler-error-c2334"></a>컴파일러 오류 C2334

예기치 않은 토큰이 있습니다. 위의 ': 또는 {'; 명백한 함수 본문을 건너뜁니다.

다음 샘플 C2334를 생성합니다. 이 오류는 오류 C2059 후 발생합니다.

```
// C2334.cpp
// compile with: /c
// C2059 expected
struct s1 {
   s1   {}   // C2334
   s1() {}   // OK
};
```