---
title: 컴파일러 오류 C2824
ms.date: 11/04/2016
f1_keywords:
- C2824
helpviewer_keywords:
- C2824
ms.assetid: 5bd865f7-e0af-404e-80fe-e2b798b44a59
ms.openlocfilehash: 226fc078312a214c561e80064474ee237245c0f8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50559980"
---
# <a name="compiler-error-c2824"></a>컴파일러 오류 C2824

'operator new' 이어야 합니다 반환 형식은 ' void *'

연산자의 오버 로드 기반이 아닌 포인터를 사용 하 여 `new` 돌아가야 `void *`합니다.

다음 샘플에서는 C2824 오류가 생성 됩니다.

```
// C2824.cpp
// compile with: /c
class   A {
   A* operator new(size_t i, char *m);   // C2824
   // try the following line instead
   // void* operator new(size_t i, char *m);
};
```