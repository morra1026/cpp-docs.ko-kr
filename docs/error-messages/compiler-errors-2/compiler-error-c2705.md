---
title: 컴파일러 오류 C2705
ms.date: 11/04/2016
f1_keywords:
- C2705
helpviewer_keywords:
- C2705
ms.assetid: 29249ea3-4ea7-4105-944b-bdb83e8d6852
ms.openlocfilehash: 872471158d3f8c301a271dd68b2ef36839e2b9c5
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50616273"
---
# <a name="compiler-error-c2705"></a>컴파일러 오류 C2705

'label': '예외 핸들러 블록' 범위로 잘못 점프 했습니다

실행 내에서 레이블로 점프를 `try` / `catch`, `__try` / `__except`하십시오 `__try` / `__finally` 블록. 자세한 내용은 [예외 처리](../../cpp/exception-handling-in-visual-cpp.md)를 참조하세요.

다음 샘플에서는 C2705 오류가 생성 됩니다.

```
// C2705.cpp
int main() {
goto trouble;
   __try {
      trouble: ;   // C2705
   }
   __finally {}

   // try the following line instead
   // trouble: ;
}
```