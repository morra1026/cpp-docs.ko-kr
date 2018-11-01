---
title: 컴파일러 오류 C2344
ms.date: 11/04/2016
f1_keywords:
- C2344
helpviewer_keywords:
- C2344
ms.assetid: a84c7b37-c84e-4345-8691-c23abb2dc193
ms.openlocfilehash: d1ba3a0f975dbc96c9c6ca51a8dac89b5a614572
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50439484"
---
# <a name="compiler-error-c2344"></a>컴파일러 오류 C2344

align(#): 맞춤은 2의 거듭제곱이어야 합니다.

[align](../../cpp/align-cpp.md) 키워드를 사용하는 경우 전달하는 값이 2의 거듭제곱이어야 합니다.

예를 들어 3은 2의 거듭제곱이 아니므로 다음 코드는 C2344를 생성합니다.

```
// C2344.cpp
// compile with: /c
__declspec(align(3)) int a;   // C2344
__declspec(align(4)) int b;   // OK
```