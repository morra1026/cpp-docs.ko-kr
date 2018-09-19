---
title: 컴파일러 오류 C2808 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2808
dev_langs:
- C++
helpviewer_keywords:
- C2808
ms.assetid: 3d745102-d3b3-4735-a7d2-ad42d5bf3cfa
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: e4d256fd07f717137f6afe890884f3c1f54944ec
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46055925"
---
# <a name="compiler-error-c2808"></a>컴파일러 오류 C2808

단항 'operator o'에 정식 매개 변수가 너무 많습니다.

단항 연산자에는 비 void 매개 변수 목록이 있습니다.

다음 샘플에서는 C2808를 생성합니다.

```
// C2808.cpp
// compile with: /c
class X {
public:
   X operator! ( X );   // C2808 nonvoid parameter list
   X operator! ( void );   // OK
};

```