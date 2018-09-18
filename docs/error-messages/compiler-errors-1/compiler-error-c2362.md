---
title: 컴파일러 오류 C2362 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2362
dev_langs:
- C++
helpviewer_keywords:
- C2362
ms.assetid: 7aafecbc-b3cf-45a6-9ec3-a17e3f222511
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: f78b850f95614255fed372570742a0f88a9e30e2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46035983"
---
# <a name="compiler-error-c2362"></a>컴파일러 오류 C2362

'identifier' 초기화가 'goto 레이블' 의해 생략 되었습니다.

사용 하 여 컴파일하면 [/Za](../../build/reference/za-ze-disable-language-extensions.md)에서 레이블로 점프 식별자를 초기화할 수 없습니다.

를 입력 하지 않으면 하는 블록에서 선언 묶입니다 않으면 이니셜라이저를 사용 하는 선언이 점프할 수 없습니다 또는 변수가 이미 초기화 되었습니다.

다음 샘플에서는 C2326을 생성합니다.

```
// C2362.cpp
// compile with: /Za
int main() {
   goto label1;
   int i = 1;      // C2362, initialization skipped
label1:;
}
```

해결 방법:

```
// C2362b.cpp
// compile with: /Za
int main() {
   goto label1;
   {
      int j = 1;   // OK, this block is never entered
   }
label1:;
}
```