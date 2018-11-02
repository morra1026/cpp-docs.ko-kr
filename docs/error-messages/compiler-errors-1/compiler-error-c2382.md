---
title: 컴파일러 오류 C2382
ms.date: 11/04/2016
f1_keywords:
- C2382
helpviewer_keywords:
- C2382
ms.assetid: 4d4436f9-d0d6-4bd0-b8ec-767b89adfb2f
ms.openlocfilehash: 4115a01f9e4dcab31a05bb3994109e97694121e6
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50593070"
---
# <a name="compiler-error-c2382"></a>컴파일러 오류 C2382

'function': 재정의. 예외 사양이 다릅니다.

[/Za](../../build/reference/za-ze-disable-language-extensions.md)아래에서 이 오류는 함수 오버로드가 [예외 사양](../../cpp/exception-specifications-throw-cpp.md)에서만 시도되었음을 나타냅니다.

다음 샘플에서는 C2382를 생성합니다.

```
// C2382.cpp
// compile with: /Za /c
void f1(void) throw(int) {}
void f1(void) throw(char) {}   // C2382
void f2(void) throw(char) {}   // OK
```