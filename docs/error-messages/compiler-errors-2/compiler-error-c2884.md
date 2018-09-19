---
title: 컴파일러 오류 C2884 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2884
dev_langs:
- C++
helpviewer_keywords:
- C2884
ms.assetid: 8b4d43e3-3fb5-4360-86c8-de59d8736d4f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9d9266162d4608e39982cce1e94751e427bc5e47
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46054716"
---
# <a name="compiler-error-c2884"></a>컴파일러 오류 C2884

'name': using 선언 충돌 로컬 function '함수를 사용 하 여에서 도입 된

함수를 두 번 이상 정의 하려고 했습니다. 첫 번째 정의 로컬 정의입니다. 두 번째는 사용 하 여 네임 스페이스에서는 `using` 선언 합니다.

다음 샘플에서는 C2884 오류가 생성 됩니다.

```
// C2884.cpp
namespace A {
   void z(int);
}

void f() {
   void z(int);
   using A::z;   // C2884 z is already defined
}
```