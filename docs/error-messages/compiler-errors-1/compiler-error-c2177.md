---
title: 컴파일러 오류 C2177
ms.date: 11/04/2016
f1_keywords:
- C2177
helpviewer_keywords:
- C2177
ms.assetid: 2a39a880-cddb-4d3e-a572-645a14c4c478
ms.openlocfilehash: 9beb8454804401f8b39f9976fe62faf6e2659537
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50641134"
---
# <a name="compiler-error-c2177"></a>컴파일러 오류 C2177

상수가 너무 큽니다.

상수 값이 할당된 변수 형식에 대해 너무 큽니다.

다음 샘플에서는 C2177을 생성합니다.

```
// C2177.cpp
int main() {
   int a=18446744073709551616;   // C2177
   int b=18446744073709551615;   // OK
}
```