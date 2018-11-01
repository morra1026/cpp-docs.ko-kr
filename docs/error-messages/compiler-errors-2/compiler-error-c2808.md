---
title: 컴파일러 오류 C2808
ms.date: 11/04/2016
f1_keywords:
- C2808
helpviewer_keywords:
- C2808
ms.assetid: 3d745102-d3b3-4735-a7d2-ad42d5bf3cfa
ms.openlocfilehash: 7b40a81748748a7566a8c1e6add84121f8925895
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50572018"
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