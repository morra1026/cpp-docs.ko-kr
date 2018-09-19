---
title: 컴파일러 경고 (수준 1) C4186 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4186
dev_langs:
- C++
helpviewer_keywords:
- C4186
ms.assetid: caf3f7d8-f305-426b-8d4e-2b96f5c269ea
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0bfc722a07d2ddb10e5be8c6d8fde60956b297c8
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46079780"
---
# <a name="compiler-warning-level-1-c4186"></a>컴파일러 경고(수준 1) C4186

\#가져오기 ' attribute '특성에 count 인수가; 필요 무시

`#import` 특성의 인수 개수가 잘못되었습니다.

## <a name="example"></a>예제

```
// C4186.cpp
// compile with: /W1 /c
#import "stdole2.tlb" no_namespace("abc") rename("a","b","c")  // C4186
```

`no_namespace` 특성은 인수를 사용하지 않습니다. **rename** 특성은 두 개의 인수만 사용합니다.