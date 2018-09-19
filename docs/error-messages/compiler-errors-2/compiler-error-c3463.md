---
title: 컴파일러 오류 C3463 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3463
dev_langs:
- C++
helpviewer_keywords:
- C3463
ms.assetid: 153efcc0-085c-4615-84ea-d22942618bdf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2169897a3ad4a6d2d78f22b7ea323d70020e1b12
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46036620"
---
# <a name="compiler-error-c3463"></a>컴파일러 오류 C3463

'type': 형식을 'implements' 특성에 사용할 수 없습니다.

잘못 된 형식에 전달 된 합니다 [구현](../../windows/implements-cpp.md) 특성입니다. 예를 들어 `implements`에 인터페이스를 전달할 수 있지만 포인터를 인터페이스에 전달할 수는 없습니다.

## <a name="example"></a>예제

다음 샘플에서는 C3463을 생성합니다.

```
// C3463.cpp
// compile with: /c
#include <windows.h>
[object, uuid("00000000-0000-0000-0000-000000000001")]
__interface X {};

typedef X* PX;

[ coclass, uuid("00000000-0000-0000-0000-000000000002"), implements(interfaces=PX) ]   // C3463
// try the following line instead
// [ coclass, uuid("00000000-0000-0000-0000-000000000002"), implements(interfaces=X) ]
class CMyClass : public X {};
```