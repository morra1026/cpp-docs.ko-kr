---
title: 컴파일러 경고(수준 1) C4615
ms.date: 11/04/2016
f1_keywords:
- C4615
helpviewer_keywords:
- C4615
ms.assetid: 7b107c01-0da2-4e01-8b40-93813e30b94c
ms.openlocfilehash: 1032261c39e0a285ac686e09573161de3b46e0e5
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50573519"
---
# <a name="compiler-warning-level-1-c4615"></a>컴파일러 경고(수준 1) C4615

\#pragma 경고: 알 수 없는 사용자 경고 형식

잘못 된 경고 지정자를 사용한 **pragma** [경고](../../preprocessor/warning.md)합니다. 오류를 해결 하려면 올바른 경고 지정자를 사용 합니다.

다음 샘플에서는 C4615 오류가 생성 됩니다.

```
// C4615.cpp
// compile with: /W1 /LD
#pragma warning(enable : 4401)   // C4615, 'enable' not valid specifier

// use the code below to resolve the error
// #pragma warning(default : 4401)
```