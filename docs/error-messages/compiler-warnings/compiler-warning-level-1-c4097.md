---
title: 컴파일러 경고 (수준 1) C4097 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4097
dev_langs:
- C++
helpviewer_keywords:
- C4097
ms.assetid: 2525be51-fac2-43b2-b57c-3bbf1a2268f7
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 93202696c06a38682da95947ac068b2d90e177ec
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46062685"
---
# <a name="compiler-warning-level-1-c4097"></a>컴파일러 경고 (수준 1) C4097

pragma 매개 변수는 'restore' 또는 'off'이어야 합니다.

Pragma에 잘못된 값이 전달되었습니다.

다음 샘플에서는 C4097을 생성합니다.

```
// C4097.cpp
// compile with: /W1
#pragma runtime_checks("",test)   // C4097
// try the following line instead
// #pragma runtime_checks("",off)

int main() {
}
```