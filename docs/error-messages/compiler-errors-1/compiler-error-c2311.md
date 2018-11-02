---
title: 컴파일러 오류 C2311
ms.date: 11/04/2016
f1_keywords:
- C2311
helpviewer_keywords:
- C2311
ms.assetid: 1aff9bd5-ed0b-4db6-bbc0-01ac89850cf2
ms.openlocfilehash: f4eff6f88a247dd17a2c9399b9009717f8fb8e62
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50444073"
---
# <a name="compiler-error-c2311"></a>컴파일러 오류 C2311

'exception': '...' 줄 번호에 의해 포착 됩니다

줄임표 (...)에 대 한 catch 처리기는 throw에 대해 마지막 처리기 여야 합니다.

다음 샘플에서는 C2311를 생성합니다.

```
// C2311.cpp
// compile with: /EHsc
#include <eh.h>
int main() {
   try {
      throw "ooops!";
   }
   catch( ... ) {}
   catch( int ) {}   // C2311  ellipsis handler not last catch
}
```