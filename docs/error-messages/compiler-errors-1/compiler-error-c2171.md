---
title: 컴파일러 오류 C2171 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2171
dev_langs:
- C++
helpviewer_keywords:
- C2171
ms.assetid: a80343b5-ab3f-4413-b6f1-3ce9d7e519e5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a5c2e3c87db5a82cc3606ebca049a35adec5fa61
ms.sourcegitcommit: 913c3bf23937b64b90ac05181fdff3df947d9f1c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/18/2018
ms.locfileid: "46029249"
---
# <a name="compiler-error-c2171"></a>컴파일러 오류 C2171

'operator': 'type' 형식의 피연산자에는 맞지 않습니다.

단항 연산자가 잘못된 피연산자 형식과 함께 사용됩니다.

## <a name="example"></a>예제

다음 샘플에서는 C2171을 생성합니다.

```
// C2171.cpp
int main() {
   double d, d1;
   d = ~d1;   // C2171

   // OK
   int d2 = 0, d3 = 0;
   d2 = ~d3;
}
```

## <a name="example"></a>예제

다음 샘플에서는 C2171을 생성합니다.

```
// C2171_b.cpp
// compile with: /c
class A {
public:
   A() { STF( &A::D ); }

   void D() {}
   void DTF() {
      (*TF)();   // C2171
      (this->*TF)();   // OK
   }

   void STF(void (A::*fnc)()) {
      TF = fnc;
   }

private:
   void (A::*TF)();
};
```