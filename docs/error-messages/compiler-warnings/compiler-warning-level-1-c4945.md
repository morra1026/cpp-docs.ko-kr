---
title: 컴파일러 경고 (수준 1) C4945 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4945
dev_langs:
- C++
helpviewer_keywords:
- C4945
ms.assetid: 6d2079ea-dc59-4611-bc68-9a22c06f7587
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 48797667c880bcd441065da3651adabdb955b52b
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46027520"
---
# <a name="compiler-warning-level-1-c4945"></a>컴파일러 경고(수준 1) C4945

'symbol': 'assembly2'에서 기호를 가져올 수 없습니다: 'symbol' 어셈블리가 'assembly1'에서 이미 가져온 대로

기호가 참조 된 어셈블리에서 가져온 하지만 해당 기호를 다른 참조 된 어셈블리에서 이미 가져왔습니다. 중 하나는 어셈블리 중 하나를 참조 하지 않거나 어셈블리 중 하나에서 변경 기호 이름을 가져옵니다.

다음 샘플에서는 C4945 생성 합니다.

```
// C4945a.cs
// compile with: /target:library
// C# source code to create a dll
public class ClassA {
   public int i;
}
```

그런 다음

```
// C4945b.cs
// compile with: /target:library
// C# source code to create a dll
public class ClassA {
   public int i;
}
```

그런 다음

```
// C4945c.cpp
// compile with: /clr /LD /W1
#using "C4945a.dll"
#using "C4945b.dll"   // C4945
```