---
title: 컴파일러 오류 C2182
ms.date: 11/04/2016
f1_keywords:
- C2182
helpviewer_keywords:
- C2182
ms.assetid: dfd8d47d-9606-496e-bd96-4bf41ba1f857
ms.openlocfilehash: 3c33e722143c15c566d96226429adbb8868b34ca
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50598434"
---
# <a name="compiler-error-c2182"></a>컴파일러 오류 C2182

'identifier': 'void' 형식을 잘못 사용했습니다.

변수가 선언된 형식 `void`입니다.

다음 샘플에서는 C2182를 생성합니다.

```
// C2182.cpp
// compile with: /c
int main() {
   int i = 10;
   void &ir = i;   // C2182 cannot have a reference to type void
   int &ir = i;   // OK
}
```