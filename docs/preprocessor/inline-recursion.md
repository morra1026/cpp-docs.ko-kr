---
title: inline_recursion
ms.date: 11/04/2016
f1_keywords:
- inline_recursion_CPP
- vc-pragma.inline_recursion
helpviewer_keywords:
- pragmas, inline_recursion
- inline_recursion pragma
ms.assetid: cfef5791-63b7-45ac-9574-623747b9b9c9
ms.openlocfilehash: 635d33d91e779d88b56e353d0cddf6b34b313855
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50523850"
---
# <a name="inlinerecursion"></a>inline_recursion
직접 또는 상호 재귀 함수 호출의 인라인 확장을 제어합니다.

## <a name="syntax"></a>구문

```
#pragma inline_recursion( [{on | off}] )
```

## <a name="remarks"></a>설명

로 표시 된이 pragma 제어 함수를 사용 [인라인](../cpp/inline-functions-cpp.md) 하 고 [__inline](../cpp/inline-functions-cpp.md) 컴파일러에서 자동으로 확장 되는 함수나는 `/Ob2` 옵션입니다. 이 pragma 사용 하려면 프로그램 [/Ob](../build/reference/ob-inline-function-expansion.md) 1 또는 2 컴파일러 옵션 설정입니다. 기본 상태로 **inline_recursion** 꺼져 있습니다. 이 pragma는 pragma가 표시된 후 첫 번째 함수에서 적용되며 함수의 정의에는 영향을 미치지 않습니다.

합니다 **inline_recursion** pragma는 재귀 함수가 확장 되는 방식을 제어 합니다. 하는 경우 **inline_recursion** 해제 되어 있고 인라인 함수 자체 (직접 또는 간접적으로), 함수를 호출 하는 경우 한 번만 확장된 됩니다. 경우 **inline_recursion** 켜져 함수를 사용 하 여 설정 된 값에 도달할 때까지 여러 번 확장 되는 [inline_depth](../preprocessor/inline-depth.md) pragma에는 정의한재귀함수에대한기본값`inline_depth` pragma에 또는 용량을 제한 합니다.

## <a name="see-also"></a>참고 항목

[Pragma 지시문 및 __Pragma 키워드](../preprocessor/pragma-directives-and-the-pragma-keyword.md)<br/>
[inline_depth](../preprocessor/inline-depth.md)<br/>
[/Ob(인라인 함수 확장)](../build/reference/ob-inline-function-expansion.md)