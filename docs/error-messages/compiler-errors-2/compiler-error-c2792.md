---
title: 컴파일러 오류 C2792 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2792
dev_langs:
- C++
helpviewer_keywords:
- C2792
ms.assetid: 392cf748-4f5e-4e62-a364-3118d5658408
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1a334cce79b13dfe5155de06e42ce998406978f6
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46062893"
---
# <a name="compiler-error-c2792"></a>컴파일러 오류 C2792

'super':이 키워드 뒤에 야 ': '

키워드 다음에 올 수 있는 토큰 `__super` 는 `::`합니다.

다음 샘플에서는 C2792를 생성합니다.

```
// C2792.cpp
struct B {
   void mf();
};

struct D : B {
   void mf() {
      __super.();   // C2792

      // try the following line instead
      // __super::mf();
   }
};
```