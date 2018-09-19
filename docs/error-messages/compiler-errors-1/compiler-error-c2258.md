---
title: 컴파일러 오류 C2258 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2258
dev_langs:
- C++
helpviewer_keywords:
- C2258
ms.assetid: 105eaa87-befb-4ecb-9a3f-e09e14d2f5bf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3c1d055858a4373a322175e0fda7a4c9ad4a2e05
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46022411"
---
# <a name="compiler-error-c2258"></a>컴파일러 오류 C2258

순수 구문이 잘못되었습니다. '= 0'이어야 합니다.

순수 가상 함수를 잘못된 구문으로 선언했습니다.

다음 샘플에서는 C2258을 생성합니다.

```
// C2258.cpp
// compile with: /c
class A {
public:
   void virtual func1() = 1; // C2258
   void virtual func2() = 0;   // OK
};
```