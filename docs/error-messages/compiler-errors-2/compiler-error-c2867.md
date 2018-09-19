---
title: 컴파일러 오류 C2867 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2867
dev_langs:
- C++
helpviewer_keywords:
- C2867
ms.assetid: 63be26b2-d9ab-4f3d-a8b7-981ce3e4d6b9
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ba16c619aa55636db7e52c03162446307bd8b62c
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46022255"
---
# <a name="compiler-error-c2867"></a>컴파일러 오류 C2867

'identifier': 네임 스페이스가 아닙니다

`using` 지시문은 네임 스페이스 이외의 항목에 적용 되었습니다.

다음 샘플에서는 C2867 오류가 생성 됩니다.

```
// C2867.cpp
// compile with: /c
namespace N {
   class X {};
}
using namespace N::X;   // C2867
```