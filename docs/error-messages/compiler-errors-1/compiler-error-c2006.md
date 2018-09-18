---
title: 컴파일러 오류 C2006 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2006
dev_langs:
- C++
helpviewer_keywords:
- C2006
ms.assetid: caaed6f7-ceb9-4742-8820-d66657c0b04d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e9468be17584a54047563bace2b35f5cb4888b41
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46031212"
---
# <a name="compiler-error-c2006"></a>컴파일러 오류 C2006

'directive' 파일 이름이 'token' 예상

같은 지시문 [#include](../../preprocessor/hash-include-directive-c-cpp.md) 하거나 [#import](../../preprocessor/hash-import-directive-cpp.md) 파일 이름이 필요 합니다. 이 오류를 해결 하려면 *토큰* 유효한 파일 이름이 됩니다. 또한 큰따옴표 또는 꺾쇠 괄호에 파일을 배치 합니다.

다음 샘플에서는 C2006 오류가 생성 됩니다.

```
// C2006.cpp
#include stdio.h   // C2006
```

해결 방법:

```
// C2006b.cpp
// compile with: /c
#include <stdio.h>
```