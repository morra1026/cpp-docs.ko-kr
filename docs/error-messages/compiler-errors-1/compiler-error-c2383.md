---
title: 컴파일러 오류 C2383
ms.date: 11/04/2016
f1_keywords:
- C2383
helpviewer_keywords:
- C2383
ms.assetid: 6696221d-879c-477a-a0f3-a6edc15fd3d7
ms.openlocfilehash: 06d4c19208bd242169e1cd07a71e8a568f46f7b1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50466094"
---
# <a name="compiler-error-c2383"></a>컴파일러 오류 C2383

'*기호*':이 기호에 기본 인수를 사용할 수 없습니다

C + + 컴파일러는 함수에 대 한 포인터에 기본 인수를 허용 하지 않습니다.

이 코드는 Visual Studio 2005 이전 버전의 Visual c + + 컴파일러에서 허용 된 하지만 이제 오류를 제공 합니다. Visual c + +의 모든 버전에서 작동 하는 코드에 대 한 함수에 대 한 포인터 인수에 기본값을 할당 하지 마십시오.

## <a name="example"></a>예제

다음 예제에서는 C2383를 생성 하 고 가능한 솔루션을 보여 줍니다.

```cpp
// C2383.cpp
// compile with: /c
void (*pf)(int = 0);   // C2383
void (*pf)(int);   // OK
```