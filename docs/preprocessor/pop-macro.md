---
title: pop_macro
ms.date: 11/04/2016
f1_keywords:
- vc-pragma.pop_macro
- pop_macro_CPP
helpviewer_keywords:
- pop_macro pragma
- pragmas, pop_macro
ms.assetid: 3b5489d0-69ba-4c66-b572-2748af0f12bb
ms.openlocfilehash: 28529ad0d9204034ea25fbca3696982a38889951
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50437243"
---
# <a name="popmacro"></a>pop_macro
값을 설정 합니다 *macro_name* 매크로 값이이 매크로 대 한 스택의 맨 위에 있습니다.

## <a name="syntax"></a>구문

```
#pragma pop_macro("
macro_name
")
```

## <a name="remarks"></a>설명

먼저 실행 해야 합니다는 [push_macro](../preprocessor/push-macro.md) 에 대 한 *macro_name* 수행 하기 전에 **pop_macro**합니다.

## <a name="example"></a>예제

```cpp
// pragma_directives_pop_macro.cpp
// compile with: /W1
#include <stdio.h>
#define X 1
#define Y 2

int main() {
   printf("%d",X);
   printf("\n%d",Y);
   #define Y 3   // C4005
   #pragma push_macro("Y")
   #pragma push_macro("X")
   printf("\n%d",X);
   #define X 2   // C4005
   printf("\n%d",X);
   #pragma pop_macro("X")
   printf("\n%d",X);
   #pragma pop_macro("Y")
   printf("\n%d",Y);
}
```

```Output
1
2
1
2
1
3
```

## <a name="see-also"></a>참고 항목

[Pragma 지시문 및 __Pragma 키워드](../preprocessor/pragma-directives-and-the-pragma-keyword.md)