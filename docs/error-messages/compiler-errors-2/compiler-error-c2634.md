---
title: 컴파일러 오류 C2634
ms.date: 11/04/2016
f1_keywords:
- C2634
helpviewer_keywords:
- C2634
ms.assetid: 58c8f2db-ac95-4a81-9355-ef3cfb0ba7b3
ms.openlocfilehash: 99b6ce006d91c36d6bcd58e607d2bc8946ee6e55
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50492876"
---
# <a name="compiler-error-c2634"></a>컴파일러 오류 C2634

'&class::member' : 참조 멤버에 대한 포인터가 잘못되었습니다.

참조 멤버에 대 한 포인터 선언 됩니다.

다음 샘플에서는 C2634 오류가 생성 됩니다.

```
// C2634.cpp
int mem;
struct S {
   S() : rf(mem) { }
   int &rf;
};
int (S::*pdm) = &S::rf;   // C2634
```