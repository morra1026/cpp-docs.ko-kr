---
title: 컴파일러 오류 C2443
ms.date: 11/04/2016
f1_keywords:
- C2443
helpviewer_keywords:
- C2443
ms.assetid: 315330d5-24bc-4193-a531-0642095be58f
ms.openlocfilehash: 41ae2c430362f96f5863819e2bf49124bdfb0a4d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50598474"
---
# <a name="compiler-error-c2443"></a>컴파일러 오류 C2443

피연산자 크기가 충돌 합니다.

명령에서 피연산자가 모두 동일한 크기 여야 합니다.

다음 샘플에서는 C2443를 생성합니다.

```
// C2443.cpp
// processor: x86
short var;
int main() {
   __asm xchg ax,bl   // C2443
   __asm mov al,red   // C2443
   __asm mov al,BYTE PTR var   // OK
}
```