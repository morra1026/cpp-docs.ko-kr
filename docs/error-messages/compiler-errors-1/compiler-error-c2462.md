---
title: 컴파일러 오류 C2462
ms.date: 11/04/2016
f1_keywords:
- C2462
helpviewer_keywords:
- C2462
ms.assetid: a8601bf8-f5ce-41de-9117-e2632bd4996b
ms.openlocfilehash: 0b342f8b878c48a77336fab4921cf4a668e248ab
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50607053"
---
# <a name="compiler-error-c2462"></a>컴파일러 오류 C2462

'identifier': ' new 식 '에서 형식을 정의할 수 없습니다

피연산자 필드의 형식을 정의할 수 없습니다는 `new` 연산자입니다. 별도 문에서 형식 정의 배치 합니다.

다음 샘플에서는 C2462 오류가 생성 됩니다.

```
// C2462.cpp
int main() {
   new struct S { int i; };   // C2462
}
```