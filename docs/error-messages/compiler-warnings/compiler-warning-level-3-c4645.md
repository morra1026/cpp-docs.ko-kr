---
title: 컴파일러 경고(수준 3) C4645
ms.date: 11/04/2016
f1_keywords:
- C4645
helpviewer_keywords:
- C4645
ms.assetid: fd7c1ddf-f0d0-4e10-bab9-ccb4c3476298
ms.openlocfilehash: a3e5c834a3f14b9a125176dcddd5bcc355cf1faa
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50536775"
---
# <a name="compiler-warning-level-3-c4645"></a>컴파일러 경고(수준 3) C4645

__declspec(noreturn)으로 선언된 함수에 return 문이 있습니다.

A [return](../../cpp/return-statement-in-program-termination-cpp.md) 문이 [noreturn](../../cpp/noreturn.md) `__declspec` 한정자로 표시된 함수에 있습니다. `return` 문이 무시되었습니다.

다음 샘플에서는 C4645를 생성합니다.

```
// C4645.cpp
// compile with:  /W3
void __declspec(noreturn) func() {
   return;   // C4645, delete this line to resolve
}

int main() {
}
```