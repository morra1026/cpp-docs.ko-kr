---
title: 컴파일러 오류 C2695
ms.date: 11/04/2016
f1_keywords:
- C2695
helpviewer_keywords:
- C2695
ms.assetid: 3f6f2091-c38b-40ea-ab6c-f1846f5702d7
ms.openlocfilehash: 08f74bf635324ed9a05c13ecf532862d58e4f0b1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2018
ms.locfileid: "50429421"
---
# <a name="compiler-error-c2695"></a>컴파일러 오류 C2695

'function1': 재정의 가상 함수에서 'function2'만 다른 호출 규칙

파생된 클래스에서 함수 서명의 기본 클래스의 함수를 재정의 및 호출 규칙을 변경할 수 없습니다.

다음 샘플에서는 C2695를 생성합니다.

```
// C2695.cpp
class C {
   virtual void __fastcall func();
};

class D : public C {
   virtual void __clrcall func();   // C2695
};
```