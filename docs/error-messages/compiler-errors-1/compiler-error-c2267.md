---
title: 컴파일러 오류 C2267
ms.date: 11/04/2016
f1_keywords:
- C2267
helpviewer_keywords:
- C2267
ms.assetid: ea63bebb-6208-4367-8440-39be07f9c360
ms.openlocfilehash: 5ff8b0bee1f79d9534841e4368fd5a5249cbb413
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50534851"
---
# <a name="compiler-error-c2267"></a>컴파일러 오류 C2267

'function': 블록 범위가 있는 정적 함수는 사용할 수 없습니다.

로컬 함수를 선언 `static`합니다. 정적 함수는 전역 범위를 가져야 합니다.

다음 샘플에서는 C2267 오류가 생성 됩니다.

```
// C2267.cpp
static int func2();   // OK
int main() {
    static int func1();   // C2267
}
```