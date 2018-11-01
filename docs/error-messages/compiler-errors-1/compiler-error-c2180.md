---
title: 컴파일러 오류 C2180
ms.date: 11/04/2016
f1_keywords:
- C2180
helpviewer_keywords:
- C2180
ms.assetid: ea71b39e-b977-48a7-b7bd-af68ef5e263b
ms.openlocfilehash: 16fcf15eb29743f74bbf2edcb1016f2e15228e5a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50553320"
---
# <a name="compiler-error-c2180"></a>컴파일러 오류 C2180

제어 식이 'type' 형식입니다.

`if`, `while`, `for` 또는 `do` 문의 제어 식은 `void`로 캐스팅되는 식입니다. 이 문제를 해결하려면 `bool` 또는 `bool`로 변환할 수 있는 형식을 생성하는 식으로 제어 식을 변경합니다.

다음 샘플에서는 C2180 오류가 발생하는 경우를 보여 줍니다.

```
// C2180.c

int main() {
   while ((void)1)   // C2180
      return 1;
   while (1)         // OK
      return 0;
}
```