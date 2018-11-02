---
title: 컴파일러 오류 C3738
ms.date: 11/04/2016
f1_keywords:
- C3738
helpviewer_keywords:
- C3738
ms.assetid: dd3ee011-e204-4264-bf3a-da32c4ef7038
ms.openlocfilehash: e313c7d66bc030183e330dd961fad2fb35f02ac2
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50539323"
---
# <a name="compiler-error-c3738"></a>컴파일러 오류 C3738

'calling_convention': 인스턴스화되는 템플릿의 명시적 인스턴스화의 호출 규칙이 일치 해야 합니다

명시적 인스턴스화에서 호출 규칙을 지정 하지 않으면 것이 좋습니다. 그러나 필요한 경우 호출 규칙 일치 해야 합니다.

## <a name="example"></a>예제

다음 샘플 C3738를 생성합니다.

```
// C3738.cpp
// compile with: /clr
// processor: x86
#include <stdio.h>
template< class T >
void f ( T arg ) {   // by default calling convention is __cdecl
   printf ( "f: %s\n", __FUNCSIG__ );
}

template
void __stdcall f< int > ( int arg );   // C3738
// try the following line instead
// void f< int > ( int arg );

int main () {
   f(1);
   f< int > ( 1 );
}
```