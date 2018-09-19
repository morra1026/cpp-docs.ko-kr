---
title: 컴파일러 오류 C2711 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2711
dev_langs:
- C++
helpviewer_keywords:
- C2711
ms.assetid: 9df9f808-7419-4e63-abdd-e6538ff0871f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c5a2e757c525d272055077cb95516abf42c06dbc
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46088438"
---
# <a name="compiler-error-c2711"></a>컴파일러 오류 C2711

'function': 두이 일 수 없습니다는 관리 코드로 #pragma 고려

몇 가지 지침이 하면 컴파일러가 바깥쪽 함수에 대 한 MSIL을 생성 합니다.

다음 샘플에서는 C2711 오류가 생성 됩니다.

```
// C2711.cpp
// compile with: /clr
// processor: x86
using namespace System;
value struct V {
   static const t = 10;
};

void bar() {
   V::t;
   __asm int 3   // C2711 inline asm can't be compiled managed
}
```