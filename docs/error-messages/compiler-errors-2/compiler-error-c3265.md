---
title: 컴파일러 오류 C3265
ms.date: 11/04/2016
f1_keywords:
- C3265
helpviewer_keywords:
- C3265
ms.assetid: 10ab3e17-4a9f-4120-bab5-21473869b70f
ms.openlocfilehash: a675567e23764a0b361cab4bef4bc75019de3756
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50552583"
---
# <a name="compiler-error-c3265"></a>컴파일러 오류 C3265

관리 되는 '관리 되는 구문'는 관리 되지 않는 '관리 되지 않는 구문'를 선언할 수 없습니다.

관리 되지 않는 컨텍스트에서 관리 되는 개체를 포함할 수 없습니다.

다음 샘플에서는 c3265:

```
// C3265_2.cpp
// compile with: /clr /LD
#include <vcclr.h>

ref class A { };

class B
// try the following line instead
// ref class B
{
   A ^a;   // C3265
   // or embed the managed handle using gcroot
   // try the following line instead
   // gcroot<A^> a;
};
```
