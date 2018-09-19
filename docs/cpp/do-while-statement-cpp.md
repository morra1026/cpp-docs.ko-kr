---
title: 수행할-while 문 (c + +) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- do_cpp
dev_langs:
- C++
helpviewer_keywords:
- do keyword [C++], do-while
- do-while keyword [C++]
- do keyword [C++]
- while keyword [C++], do-while
ms.assetid: e01e6f7c-7da1-4591-87f9-c26ff848e7b0
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 37155be11caaee9c609a0e11ddbfeb5d62856903
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46071200"
---
# <a name="do-while-statement-c"></a>do-while 문(C++)

실행을 *문* 지정된 된 종료 조건까지 반복적으로 (합니다 *식*) 계산 결과가 0 인 합니다.

## <a name="syntax"></a>구문

```
do
   statement
while ( expression ) ;
```

## <a name="remarks"></a>설명

종료 조건은 테스트는 루프의 각 실행 후 수행 따라서 한 **수행-동안** 루프는 종료 식의 값에 따라 여러 번 실행 합니다. **do-while** 문은 문 본문 내에서 [break](../cpp/break-statement-cpp.md), [goto](../cpp/goto-statement-cpp.md) 또는 [return](../cpp/return-statement-cpp.md) 문이 실행되는 경우에도 종료될 수 있습니다.

*expression*은 산술 형식이나 포인터 형식이어야 합니다. 다음과 같이 실행됩니다.

1. 문 본문이 실행됩니다.

1. 다음으로, *expression*이 평가됩니다. *expression*이 false인 경우 **do-while** 문이 종료되고 프로그램의 다음 문으로 제어가 전달됩니다. *expression*이 true(0이 아님)인 경우에는 프로세스가 1단계부터 반복됩니다.

## <a name="example"></a>예제

다음 샘플을 참조 하십시오.는 **수행-동안** 문:

```cpp
// do_while_statement.cpp
#include <stdio.h>
int main()
{
    int i = 0;
    do
    {
        printf_s("\n%d",i++);
    } while (i < 3);
}
```

## <a name="see-also"></a>참고자료

[반복 문](../cpp/iteration-statements-cpp.md)<br/>
[키워드](../cpp/keywords-cpp.md)<br/>
[while 문(C++)](../cpp/while-statement-cpp.md)<br/>
[for 문(C++)](../cpp/for-statement-cpp.md)<br/>
[범위 기반 for 문(C++)](../cpp/range-based-for-statement-cpp.md)