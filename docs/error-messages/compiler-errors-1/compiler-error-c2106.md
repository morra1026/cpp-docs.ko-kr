---
title: 컴파일러 오류 C2106
ms.date: 11/04/2016
f1_keywords:
- C2106
helpviewer_keywords:
- C2106
ms.assetid: d5c91a2e-04e4-4770-8478-788b98c52a53
ms.openlocfilehash: 6a82792c8a8acfd0d397e02929a457aae8ef7050
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50507577"
---
# <a name="compiler-error-c2106"></a>컴파일러 오류 C2106

'operator': 왼쪽된 피연산자 l 값 이어야 합니다.

연산자 왼쪽 피연산자로 l-value가 있어야 합니다.

다음 샘플에서는 C2106 오류가 생성 됩니다.

```
// C2106.cpp
int main() {
   int a;
   1 = a;   // C2106
   a = 1;   // OK
}
```