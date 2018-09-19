---
title: 컴파일러 오류 C2969 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2969
dev_langs:
- C++
helpviewer_keywords:
- C2969
ms.assetid: e4ea3d66-b937-4b2c-b42a-96e03fb11579
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 796660cbefab31a58a977930537897e6c537b834
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46076933"
---
# <a name="compiler-error-c2969"></a>컴파일러 오류 C2969

구문 오류: 'symbol': 멤버 함수 정의가 '}'로 끝나야 합니다.

템플릿 멤버 함수 정의에 짝이 맞지 않는 닫는 중괄호가 있습니다.

다음 샘플에서는 C2969를 생성합니다.

```
// C2969.cpp
// compile with: /c
class A {
   int i;
public:
   A(int i) {}
};

A anA(1);

class B {
   A a;
   B() : a(anA);   // C2969
   // try the following line instead
   // B() : a(anA) {}
};
```