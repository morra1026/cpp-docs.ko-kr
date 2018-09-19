---
title: 컴파일러 오류 C2862 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2862
dev_langs:
- C++
helpviewer_keywords:
- C2862
ms.assetid: c04d8499-b799-48a1-9fb4-7902a0b0ac8e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3cfd5ee07ecd7ca1613c4e7b5584294e58aace3e
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46049789"
---
# <a name="compiler-error-c2862"></a>컴파일러 오류 C2862

'interface': 인터페이스는 공용 멤버를 하나만 사용할 수 있습니다

보호 되 고 private 멤버는 다른 멤버 함수 에서만에서 액세스할 수 있습니다. 이러한 멤버 인터페이스에서 사용 되지 않으므로 해당 멤버에 대 한 구현을 제공 하지 않을 수 있습니다.

다음 샘플 C2862 생성 됩니다.

```
// C2862.cpp
// compile with: /c
#include <unknwn.h>

[object, uuid="60719E20-EF37-11D1-978D-0000F805D73B"]
__interface IMyInterface {
   HRESULT mf1(void);   // OK
protected:
   HRESULT mf2(int *b);   // C2862
private:
   HRESULT mf3(int *c);   // C2862
};
```