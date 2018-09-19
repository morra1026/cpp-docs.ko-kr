---
title: ()는 없는 코드를 생성 하지 않고 함수 이름을 사용 하 여 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- functions [C++], without parentheses
ms.assetid: edf4a177-a160-44aa-8436-e077b5b27809
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 13ca43386c9ef46f526538781a91fd1a81ade537
ms.sourcegitcommit: 92f2fff4ce77387b57a4546de1bd4bd464fb51b6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45710582"
---
# <a name="using-function-name-without--produces-no-code"></a>함수 이름을 () 없이 사용하면 코드가 생성되지 않음

프로그램에서 선언 된 함수 이름은 괄호 없이 사용 되 면 컴파일러는 코드를 생성 하지 않습니다. 이 컴파일러는 함수 주소;를 계산 하기 때문에 함수에서 매개 변수를 사용 하는 여부에 관계 없이 오류 발생 그러나 함수 호출 연산자 (")" 없기 때문에 호출이 이루어집니다. 이 결과 다음과 비슷합니다.

```
// compile with /Wall to generate a warning
int a;
a;      // no code generated here either
```

Visual c + + 경고 수준 4를 사용 해도 없는 진단 출력을 생성 합니다. 경고가 발생 하지 않습니다. 코드 없이 생성 됩니다.

아래 샘플 코드 (경고)와 함께 하 고 오류 없이 올바르게 링크 컴파일되지만 참조 코드 없이 생성 `funcn( )`합니다. 제대로 작동 하려면이 위해 함수 호출 연산자 (")"를 추가 합니다.

```
#include <stdio.h>
void funcn();

int main() {
   funcn;      /* missing function call operator;
                  call will fail.  Use funcn() */
   }

void funcn() {
   printf("\nHello World\n");
}
```

## <a name="see-also"></a>참고 항목

[코드 최적화](../../build/reference/optimizing-your-code.md)