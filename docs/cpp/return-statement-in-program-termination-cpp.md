---
title: return 문 프로그램 종료 (c + +) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- data types [C++], function return types
- function return types [C++], return statement
- return keyword [C++], syntax
ms.assetid: 66d002ab-5625-4b68-8446-71e1b8fcdbd8
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: cfcf65258767178c0f74f63ca6e938e1d940e3be
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46061138"
---
# <a name="return-statement-in-program-termination-c"></a>프로그램 종료 시 return 문 (C++)

실행을 **반환** 문을 `main` 호출 하는 기능적를 `exit` 함수. 다음 예제를 참조하세요.

```cpp
// return_statement.cpp
#include <stdlib.h>
int main()
{
    exit( 3 );
    return 3;
}
```

합니다 `exit` 하 고 **반환** 문 앞의 예제에서 기능적으로 동일 합니다. 그러나 c + +에서는 함수를 반환 형식 이외의 **void** 값을 반환 합니다. 합니다 **반환** 문을 사용 하면에서 값을 반환 하려면 `main`합니다.

## <a name="see-also"></a>참고자료

[프로그램 종료](../cpp/program-termination.md)