---
title: 컴파일러 오류 C3139 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3139
dev_langs:
- C++
helpviewer_keywords:
- C3139
ms.assetid: 95c92263-10ac-4ff3-b385-6312dd92adbc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ac401381dffab11ddb59eb05a5cafe13373d7791
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46026454"
---
# <a name="compiler-error-c3139"></a>컴파일러 오류 C3139

'struct': 멤버 없이 UDT를 내보낼 수 없습니다.

적용 하려고 합니다 [내보내기](../../windows/export.md) 특성을 빈 UDT (사용자 정의 형식)을 합니다. 예를 들어:

```
// C3139.cpp
#include "unknwn.h"
[emitidl];
[module(name=xx)];

[export] struct MyStruct {   // C3139 empty type
};
int main(){}
```