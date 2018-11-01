---
title: 컴파일러 오류 C2197
ms.date: 11/04/2016
f1_keywords:
- C2197
helpviewer_keywords:
- C2197
ms.assetid: 6dd5a6ec-bc80-41b9-a4ac-46f80eaca42d
ms.openlocfilehash: 8999edcf37277e2e05a92a6601d60d34a675719c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50527402"
---
# <a name="compiler-error-c2197"></a>컴파일러 오류 C2197

'function': 호출에 매개 변수가 너무 많습니다.

컴파일러가 함수 호출 매개 변수를 너무 많이 발견했거나 잘못된 함수 선언을 발견했습니다.

다음 샘플에서는 C2197을 생성합니다.

```
// C2197.c
// compile with: /Za /c
void func( int );
int main() {
   func( 1, 2 );   // C2197 two actual parameters
   func( 2 );   // OK
}
```