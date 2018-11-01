---
title: 컴파일러 오류 C2137
ms.date: 11/04/2016
f1_keywords:
- C2137
helpviewer_keywords:
- C2137
ms.assetid: 984687ee-7766-4f6b-ae15-0c9a010e2366
ms.openlocfilehash: 7051fbe788790f1e91a3f54720f72d8370d1e9a8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50464339"
---
# <a name="compiler-error-c2137"></a>컴파일러 오류 C2137

문자 상수가 비어 있습니다.

빈 문자 상수(' ')는 허용되지 않습니다.

다음 샘플에서는 C2137을 생성합니다.

```
// C2137.cpp
int main() {
   char c = '';   // C2137
   char d = ' ';   // OK
}
```