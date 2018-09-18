---
title: 컴파일러 오류 C2311 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2311
dev_langs:
- C++
helpviewer_keywords:
- C2311
ms.assetid: 1aff9bd5-ed0b-4db6-bbc0-01ac89850cf2
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f19e2a1b41c499605f22575f934b3d4872457011
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46065103"
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