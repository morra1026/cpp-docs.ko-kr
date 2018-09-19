---
title: 컴파일러 경고 (수준 1) C4805 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4805
dev_langs:
- C++
helpviewer_keywords:
- C4805
ms.assetid: 99c7b7e2-272e-4ab5-8580-17c42e62e2ef
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1fa9352dbd4138a755c603d332ff79232d7bb72a
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46103453"
---
# <a name="compiler-warning-level-1-c4805"></a>컴파일러 경고(수준 1) C4805

'operation': 연산에 'type' 형식과 'type' 형식을 함께 사용하는 것은 안전하지 않습니다.

이 경고는 [bool](../../cpp/bool-cpp.md) 과 [int](../../c-language/integer-types.md)간의 비교 작업에 대해 생성됩니다. 다음 샘플에서는 C4805를 생성합니다.

```
// C4805.cpp
// compile with: /W1
int main() {
   int i = 1;
   bool b = true;

   if (i == b) {   // C4805, comparing bool and int variables
   }
}
```