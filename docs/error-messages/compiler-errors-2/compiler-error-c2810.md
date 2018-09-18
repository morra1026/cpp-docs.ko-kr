---
title: 컴파일러 오류 C2810 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2810
dev_langs:
- C++
helpviewer_keywords:
- C2810
ms.assetid: f63e8f24-d7f6-42ac-904f-72ff49592ba6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 68a98d0dacf1823dd5b4f376a55279ec1e8cbff2
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46075763"
---
# <a name="compiler-error-c2810"></a>컴파일러 오류 C2810

'interface': 인터페이스는 다른 인터페이스에서 에서만 상속할 수 있습니다

[인터페이스](../../cpp/interface.md) 다른 인터페이스에서 에서만 상속할 수 있습니다 및 클래스 또는 구조체에서 상속 하지 않을 수 있습니다.

다음 샘플에서는 C2810 오류가 생성 됩니다.

```
// C2810.cpp
#include <unknwn.h>
class CBase1 {
public:
  HRESULT mf1();
  int  m_i;
};

[object, uuid="40719E20-EF37-11D1-978D-0000F805D73B"]
__interface IDerived : public CBase1 {  // C2810
// try the following line instead
// __interface IDerived {
   HRESULT mf2(void *a);
};

struct CBase2 {
   HRESULT mf1(int a, char *b);
   HRESULT mf2();
};
```