---
title: 컴파일러 오류 C2033 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2033
dev_langs:
- C++
helpviewer_keywords:
- C2033
ms.assetid: fd5a1637-9db2-4c98-a7cc-b63b39737cd9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 05ed1274f94c1df8e9654622ec059ea9707cdf87
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46043029"
---
# <a name="compiler-error-c2033"></a>컴파일러 오류 C2033

'identifier': 비트 필드에 간접 참조를 사용할 수 없습니다.

비트 필드가 허용되지 않는 포인터로 선언되었습니다.

다음 샘플에서는 C2033을 생성합니다.

```
// C2033.cpp
struct S {
   int *b : 1;  // C2033
};
```

해결 방법:

```
// C2033b.cpp
// compile with: /c
struct S {
   int b : 1;
};
```