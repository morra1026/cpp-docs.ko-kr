---
title: 컴파일러 오류 C2751
ms.date: 11/04/2016
f1_keywords:
- C2751
helpviewer_keywords:
- C2751
ms.assetid: 44a3abdf-8a87-4a09-b34b-532c220c310a
ms.openlocfilehash: 14f458725564d39851ae16b5fd2cd5a79f00420d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50470800"
---
# <a name="compiler-error-c2751"></a>컴파일러 오류 C2751

'parameter': 함수 매개 변수의 이름을 정규화 할 수 없습니다

함수 매개 변수로 정규화 된 이름을 사용할 수 없습니다.

다음 샘플에서는 C2751를 생성합니다.

```
// C2751.cpp
namespace std {
   template<typename T>
   class list {};
}

#define list std::list
void f(int &list){}   // C2751
```