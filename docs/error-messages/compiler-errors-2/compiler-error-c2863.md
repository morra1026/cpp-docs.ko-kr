---
title: 컴파일러 오류 C2863 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2863
dev_langs:
- C++
helpviewer_keywords:
- C2863
ms.assetid: 32561d67-a795-486b-b3b6-4b90a1acb176
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4df5c82a14d24a8da1d296ff6f04dd4adcd98a0f
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46136038"
---
# <a name="compiler-error-c2863"></a>컴파일러 오류 C2863

'interface': 인터페이스에 friends를 사용할 수 없습니다.

인터페이스에서 friend를 선언할 수 없습니다.

다음 샘플에서는 C2863를 생성합니다.

```
// C2863.cpp
// compile with: /c
#include <unknwn.h>

class CMyClass {
   void *f();
};

__interface IMyInterface {
   void g();

   friend int h();   // 2863
   friend interface IMyInterface1;  // C2863
   friend void *CMyClass::f();  // C2863
};
```