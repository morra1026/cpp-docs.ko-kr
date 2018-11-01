---
title: 컴파일러 오류 C3551
ms.date: 11/04/2016
f1_keywords:
- C3551
helpviewer_keywords:
- C3551
ms.assetid: c8ee23da-6568-40db-93a6-3ddb7ac47712
ms.openlocfilehash: 9dfdee155e85bd772ed1d4ce22c525f8a4c79f5c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50458749"
---
# <a name="compiler-error-c3551"></a>컴파일러 오류 C3551

"런타임에 지정된 반환 형식이 필요합니다."

`auto` 키워드를 함수 반환 형식에 대한 자리 표시자로 사용하는 경우 컴파일하면 지정되는 반환 형식을 제공해야 합니다. 다음 예제에서는 런타임에 지정된 `myFunction` 함수의 반환 형식이 `int`형식의 네 요소 배열에 대한 포인터입니다.

```
auto myFunction()->int(*)[4];
```

## <a name="see-also"></a>참고 항목

[auto](../../cpp/auto-cpp.md)