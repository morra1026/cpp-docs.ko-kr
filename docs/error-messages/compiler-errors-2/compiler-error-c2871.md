---
title: 컴파일러 오류 C2871 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2871
dev_langs:
- C++
helpviewer_keywords:
- C2871
ms.assetid: 44aeb84d-61f0-45e0-8dad-22a3cd46b7f8
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1e960dd6bc9fdf81d6a1bb127330f1066628fffd
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46117623"
---
# <a name="compiler-error-c2871"></a>컴파일러 오류 C2871

'name':이 이름의 네임 스페이스가 없습니다.

네임 스페이스를 하지 않은 식별자를 전달 하는 경우이 오류가 발생 한 [를 사용 하 여](../../cpp/namespaces-cpp.md#using_directives) 지시문입니다.

## <a name="example"></a>예제

다음 샘플에서는 C2871를 생성합니다.

```cpp
// C2871.cpp
// compile with: /c
namespace a {
   int fn(int i) { return i; }
}
namespace b {
   using namespace d;   // C2871 because d is not a namespace
   using namespace a;   // OK
}
```