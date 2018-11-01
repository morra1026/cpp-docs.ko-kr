---
title: 컴파일러 경고 (수준 1) C4162
ms.date: 11/04/2016
f1_keywords:
- C4162
helpviewer_keywords:
- C4162
ms.assetid: 21ae3c92-501d-4689-ad7d-13753cb65eff
ms.openlocfilehash: 6c6b675fd47cb6e98255515c7cd77c6dd48ea02b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50578267"
---
# <a name="compiler-warning-level-1-c4162"></a>컴파일러 경고 (수준 1) C4162

'identifier': C 링크가 있는 함수가 없습니다

C 링크가 있는 함수가 선언 되었지만 찾을 수 없습니다.

이 경고를 해결 하려면.c 파일에서 컴파일 (C 컴파일러를 호출).  C + + 컴파일러를 호출 해야 하는 경우에 extern "C" 함수 선언 전에 배치 합니다.

다음 샘플에서는 C4162

```
// C4162.cpp
// compile with: /c /W1
unsigned char _bittest(long* a, long b);
#pragma intrinsic (_bittest)   // C4162

int main() {
   bool bit;
   long num = 78002;
   bit = _bittest(&num, 5);
}
```

해결 방법:

```
// C4162b.cpp
// compile with: /c
extern "C"
unsigned char _bittest(long* a, long b);
#pragma intrinsic (_bittest)

int main() {
   bool bit;
   long num = 78002;
   bit = _bittest(&num, 5);
}
```