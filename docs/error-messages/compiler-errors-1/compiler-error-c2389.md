---
title: 컴파일러 오류 C2389
ms.date: 11/04/2016
f1_keywords:
- C2389
helpviewer_keywords:
- C2389
ms.assetid: 6122dc81-4ee3-49a5-a67d-d867808c9bac
ms.openlocfilehash: cb58ed0af3fda7ecbf399ac37758a688f014b826
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50664596"
---
# <a name="compiler-error-c2389"></a>컴파일러 오류 C2389

'operator': 'nullptr'는 잘못된 피연산자입니다.

`nullptr` 는 피연산자일 수 없습니다.

다음 샘플에서는 C2389를 생성합니다.

```
// C2389.cpp
// compile with: /clr
int main() {
   throw nullptr;   // C2389
}
```