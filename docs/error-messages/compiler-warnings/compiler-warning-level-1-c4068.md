---
title: 컴파일러 경고 (수준 1) C4068 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4068
dev_langs:
- C++
helpviewer_keywords:
- C4068
ms.assetid: 96a7397a-4eab-44ab-b3bb-36747503f7e5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 290fb0b66523771b263c1f776551362fd8da5224
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46098429"
---
# <a name="compiler-warning-level-1-c4068"></a>컴파일러 경고(수준 1) C4068

알 수 없는 pragma입니다.

컴파일러가 인식할 수 없는 [pragma](../../preprocessor/pragma-directives-and-the-pragma-keyword.md)를 무시했습니다. 사용하는 컴파일러에서 **pragma** 가 허용되는지 확인합니다. 다음 샘플에서는 C4068을 생성합니다.

```
// C4068.cpp
// compile with: /W1
#pragma NotAValidPragmaName   // C4068, use valid name to resolve
int main()
{
}
```