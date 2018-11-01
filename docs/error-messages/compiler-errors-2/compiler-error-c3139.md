---
title: 컴파일러 오류 C3139
ms.date: 11/04/2016
f1_keywords:
- C3139
helpviewer_keywords:
- C3139
ms.assetid: 95c92263-10ac-4ff3-b385-6312dd92adbc
ms.openlocfilehash: f224be74a94e0e769e7c26bc99b4790d69f6b65b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50521205"
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