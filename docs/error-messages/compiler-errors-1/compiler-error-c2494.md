---
title: 컴파일러 오류 C2494 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2494
dev_langs:
- C++
helpviewer_keywords:
- C2494
ms.assetid: 5dfd07ab-351d-49c9-b54e-f0a104776ab8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e651e66ce571ddd084c470b52494235f35f2b008
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46066806"
---
# <a name="compiler-error-c2494"></a>컴파일러 오류 C2494

'keyword' 필터 식 내에서 호출할 수 없습니다 또는 __finally/finally 블록

사용할 수 없습니다 `keyword` 에 `__finally` 또는 finally 블록입니다.

다음 샘플에서는 C2494 오류가 생성 됩니다.

```
// C2494.cpp
#include <malloc.h>

int main() {
   __try {}
   __except ( _alloca(100), 1 ) {}   // C2494
   __try {}
   __finally {
      _alloca(100);   // C2494
   }
}
```

사용 하는 경우에 C2494 발생할 수 있습니다 **/clr**합니다.

```
// C2494b.cpp
// compile with: /clr
#include <malloc.h>

int main() {
   char * buf;
   try {}
   catch (char * buf2) {}
   finally {
      _alloca(100);   // C2494
   }
}
```