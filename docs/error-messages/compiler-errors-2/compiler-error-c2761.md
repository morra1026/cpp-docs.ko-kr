---
title: 컴파일러 오류 C2761
ms.date: 11/04/2016
f1_keywords:
- C2761
helpviewer_keywords:
- C2761
ms.assetid: 38c79a05-b56d-485b-820f-95e8c0cb926f
ms.openlocfilehash: 6ad42beea28bd2070d1c7dc12086146e6ab70ff5
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50667010"
---
# <a name="compiler-error-c2761"></a>컴파일러 오류 C2761

'function': 멤버 함수 재선언 허용 되지 않습니다

멤버 함수를 다시 선언할 수 없습니다. 정의할 수 있지만 하지 다시 선언할 수 있습니다.

## <a name="example"></a>예제

다음 샘플에서는 C2761 오류가 발생 합니다.

```
// C2761.cpp
class a {
   int t;
   void test();
};

void a::a;     // C2761
void a::test;  // C2761

```

## <a name="example"></a>예제

클래스 또는 구조체의 비정적 멤버를 정의할 수 없습니다.  다음 샘플에서는 C2761 오류가 발생 합니다.

```
// C2761_b.cpp
// compile with: /c
struct C {
   int s;
   static int t;
};

int C::s;   // C2761
int C::t;   // OK
```