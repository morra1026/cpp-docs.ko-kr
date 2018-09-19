---
title: 컴파일러 경고 (수준 1) C4162 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4162
dev_langs:
- C++
helpviewer_keywords:
- C4162
ms.assetid: 21ae3c92-501d-4689-ad7d-13753cb65eff
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a36fa6a63443bf2272df7ce6125fd77afedf100f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46027182"
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