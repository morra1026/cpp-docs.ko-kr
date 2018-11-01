---
title: STACKSIZE
ms.date: 11/04/2016
f1_keywords:
- STACKSIZE
helpviewer_keywords:
- STACKSIZE .def file statement
ms.assetid: 4d8c79bd-1cb4-4e4d-90f2-b5a7a4d20e7a
ms.openlocfilehash: de2aa99375f588d682b714632590ba8e0db8ddcb
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50597225"
---
# <a name="stacksize"></a>STACKSIZE

스택 크기를 바이트 단위로 설정합니다.

```
STACKSIZE reserve[,commit]
```

## <a name="remarks"></a>설명

해당 스택 설정 방법은 합니다 [스택 할당](../../build/reference/stack-stack-allocations.md) (/stack) 옵션입니다. 에 대 한 세부 정보에 대해이 옵션에 대 한 설명서를 참조 합니다 *예약할* 및 `commit` 인수.

이 옵션은 Dll에 대 한 영향을 주지 않습니다.

## <a name="see-also"></a>참고 항목

[모듈 정의 문의 규칙](../../build/reference/rules-for-module-definition-statements.md)