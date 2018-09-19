---
title: 컴파일러 오류 C2805 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2805
dev_langs:
- C++
helpviewer_keywords:
- C2805
ms.assetid: c997dc56-e199-442f-b94e-ac551ec9b015
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ad07ea30d4124c0655e739e0e9222b3dc428a0a7
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46032239"
---
# <a name="compiler-error-c2805"></a>컴파일러 오류 C2805

이항 'operator o'에 매개 변수가 너무 적습니다.

이항 연산자 매개 변수가 없습니다.

다음 샘플에서는 C2805 오류가 생성 됩니다.

```
// C2805.cpp
// compile with: /c
class X {
public:
   X operator< ( void );   // C2805 must take one parameter
   X operator< ( X );   // OK
};
```